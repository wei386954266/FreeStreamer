FreeStreamer



// 




    
    
    //使用
    
    使用
     @property(nonatomic,strong)FSAudioStream * audioStream;
    -(void)loadPlayer{
    if (!_audioStream) {
       _audioStream = [[FSAudioStream alloc] init];
    }
    //播放失败的回调
    _audioStream.onFailure = ^(FSAudioStreamError error,NSString *description){
        NSLog(@"播放过程中发生错误，错误信息：%@",description);
    };
    
    
    // 播放完成的回调
    _audioStream.onCompletion=^(){
        NSLog(@"播放完成!");
    };
    // 设置音量
    [_audioStream setVolume:0.5];
    // 使用音频链接URL播放音频
     

    
    } 
    NSString *urlStr = [NSString stringWithFormat:@"http://xiaohe.sjs.com.cn%@",model.file_url];
          NSURL *url = [NSURL URLWithString:urlStr];
         [_audioStream playFromURL:url];
         [_audioStream play];
        [_audioStream pause];
    
 
         
