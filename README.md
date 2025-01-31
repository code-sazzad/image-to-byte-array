# image-to-byte-array

    private void image_to_byte_array(){
        BitmapDrawable bitmapDrawable= (BitmapDrawable) logo.getDrawable();
        Bitmap bitmap=bitmapDrawable.getBitmap();
        ByteArrayOutputStream byteArrayOutputStream=new ByteArrayOutputStream();
        bitmap.compress(Bitmap.CompressFormat.JPEG,50,byteArrayOutputStream);
        byte[] data=byteArrayOutputStream.toByteArray();

        String ip=Base64.encodeToString(data,Base64.DEFAULT);

        tvdisplay.setText(ip);
        //send to server button clicked
    }
