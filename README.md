# imagepreview
图片预览器
1.使用方法
Intent intent = new Intent(getContext(), PhotoPreviewActivity.class);
             intent.putStringArrayListExtra(PhotoPreviewActivity.EXTRA_PHOTOS, filePath);
             intent.putExtra(PhotoPreviewActivity.EXTRA_CURRENT_ITEM, currentIndex);
 最新结果在onActivityResult获取，可能数量比传入的数组少（因为预览器里面可以删除图片）            
List<String> newFilePathList = (List<String>) data.getSerializableExtra(PhotoPreviewActivity.EXTRA_RESULT);

由于偷懒所以直接从某个开源项目里面把这个预览器剥离出来了
原项目:com.lidong.photopicker