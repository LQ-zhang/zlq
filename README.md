
// 沙盒路径
- (NSString *)appendDocumentDir {
    
    NSString *dir = [NSSearchPathForDirectoriesInDomains(NSDocumentDirectory, NSUserDomainMask, YES) lastObject];
    
    return [dir stringByAppendingPathComponent:self.lastPathComponent];
}

- (NSString *)appendCacheDir {
    NSString *dir = [NSSearchPathForDirectoriesInDomains(NSCachesDirectory, NSUserDomainMask, YES) lastObject];
    
    return [dir stringByAppendingPathComponent:self.lastPathComponent];
}

- (NSString *)appendTmpDir {
    return [NSTemporaryDirectory() stringByAppendingPathComponent:self.lastPathComponent];
}
