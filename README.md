# Deflecting Adversarial Attacks with Pixel Deflection

Code for paper: https://arxiv.org/abs/1801.08926

## Example

» python main.py -image images/n02443114_00000055.png -map maps/n02443114_00000055.png                                                                                        20:06:33 on 2018-01-28
Image: images/n02443114_00000055.png, True Class: 'polecat'
Before Defense ----------------
Predicted Class [(u'black-footed_ferret', 0.97667706), (u'weasel', 0.012244679), (u'polecat', 0.0081524383), (u'hamster', 0.0025866854), (u'mink', 0.00027122154)]
After Defense -----------------
Predicted Class [(u'polecat', 0.58065307), (u'black-footed_ferret', 0.35132107), (u'weasel', 0.020193988), (u'hamster', 0.0084857652), (u'mink', 0.0062040896)]


## Usage

### Single image

» python main.py -image <image_path> -map <map_path>


### Batch usage

» python main.py --process_batch --directory <directory_containing_images>

In batch usage the map file is expected to have same name as image file but inside './maps' directory


To generate map see this https://github.com/iamaaditya/image-compression-cnn/blob/master/generate_map.py


### Detailed usage

» python main.py --help
  -h, --help            show this help message and exit
  -image IMAGE
  -map MAP
  -directory DIRECTORY
  --process_batch
  -classifier CLASSIFIER
                        options: resnet50, inception_v3, vgg19, xception
  -denoiser DENOISER    options: wavelet, TVM, bilateral, deconv, NLM
  -batch_size BATCH_SIZE
  -sigma SIGMA
  -window WINDOW
  -deflections DEFLECTIONS
