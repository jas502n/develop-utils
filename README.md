            File file = new File(sourcePath);
            FileInputStream fis = new FileInputStream(file);
            String picStr = IOUtils.toString(fis, "ISO8859-1");
            // des解密
            RealNameMsDesPlus desPlus = new RealNameMsDesPlus(picKey);
            String picStrDecode = desPlus.decrypt(picStr);