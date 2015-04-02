dependencies {
    //单文件依赖
    compile files('libs/commons-beanutils-1.8.0.jar')

    //某个文件夹下面全部依赖
    compile fileTree(dir: 'libs', include: '*.jar')
}
