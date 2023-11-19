# 시각화 실행하는 법
- `poetry`를 설치하여 필요한 패키지를 설치합니다
- `./visualization/` 으로 이동해서 스크립트를 실행합니다

```bash
poetry init
poetry shell

cd ./visualization/
python visualization.py --manga109_root_dir /home/dev/szmc/szmc.v1/ofs/manga109/ --book ARMS --page_index 5
```
그러면 `./visualization/out.jpg`에 시각화 결과가 나옵니다. text bbox만 출력하도록 코드를 바꿔뒀습니다.


옵션 설명
```
--manga109_root_dir     manga109디렉토리 경로 
--book                  만화타이틀이름  
--page_index            manga109/타이틀/인덱스.jpg
```


# Manga109 Demos

This repository is a collection of demo codes for the [Manga109 dataset](http://www.manga109.org/en/).

Manga109 is the largest dataset for manga (Japanese comic) images,
that is made publicly available for academic research purposes with proper copyright notation.

To download images/annotations of Manga109, please visit [this website](http://www.manga109.org/en/download.html) and send an application via the form.
You will then receive a password for downloading the images (109 titles of manga
as jpeg files)
and their annotations (bounding box coordinates of face, body, frame, and speech balloon with texts,
in the form of XML).

Please see [manga109api](https://github.com/manga109/manga109api) as well when using the dataset.

## Contents

- Annotation visualization demo - `./visualization`
- Bounding box cropping demo - `./extraction`
- MSCOCO format conversion - `./coco-format-conversion`


## Citations
When you make use of images in Manga109, please cite the following paper:

    @article{mtap_matsui_2017,
        author={Yusuke Matsui and Kota Ito and Yuji Aramaki and Azuma Fujimoto and Toru Ogawa and Toshihiko Yamasaki and Kiyoharu Aizawa},
        title={Sketch-based Manga Retrieval using Manga109 Dataset},
        journal={Multimedia Tools and Applications},
        volume={76},
        number={20},
        pages={21811--21838},
        doi={10.1007/s11042-016-4020-z},
        year={2017}
    }

When you use annotation data of Manga109, please cite the following paper:

    @article{multimedia_aizawa_2020,
        author={Kiyoharu Aizawa and Azuma Fujimoto and Atsushi Otsubo and Toru Ogawa and Yusuke Matsui and Koki Tsubota and Hikaru Ikuta},
        title={Building a Manga Dataset ``Manga109'' with Annotations for Multimedia Applications},
        journal={IEEE MultiMedia},
        volume={27},
        number={2},
        pages={8--18},
        doi={10.1109/mmul.2020.2987895},
        year={2020}
    }
