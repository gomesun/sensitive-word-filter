# sensitive-word-filter-fix

    https://github.com/hailin0/sensitive-word-filter
            这里只是针对作者的bug做下修复，其他都是fork作者。感谢作者的share。

	敏感词处理器，支持返回敏感词，高亮敏感词，替换敏感词等操作,算法为trie树实现，查找速度快。演示效果如下：
 ![Alt 演示效果](/doc/20160523233326.png "演示效果")


# 代码示例
    /**
     * bug fix, 关键字互相包含，也能正确搜索出来。 gomesun
     */
    public static void test3() {
        Set<KeyWord> kws = new HashSet<KeyWord>();
        kws.add(new KeyWord("中"));
        kws.add(new KeyWord("中国"));
        kws.add(new KeyWord("中国人"));
        kws.add(new KeyWord("国人"));
        KWSeeker kwSeeker = new KWSeeker(kws);
        List<SensitiveWordResult> findWords = kwSeeker.findWords("我是中国人来的，真的是中国人来的");
        System.out.println(findWords);
    }


# 使用方法
	https://github.com/hailin0/sensitive-word-filter



