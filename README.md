# UIView-Extension
功能1：直接修改frame中的值。包括x，y，width，height，origin，centerx，centery；

            例：
                 view.x = 50;
                 view.centerX = 100;
                 view.y = 650;
                 view.width = 200;

功能2：给UIButton设置各属性，包括frame、textLabel.font、textAlignment（此属性因没有提示，不推荐使用）以及四种状态下（nomal，hightlighted，selected，disabled）的image、title、titleColor、backgroudImage 的设置：

      例：设置nomal状态下的属性
             UIButton *btn1 = [[UIButton alloc]init];
             btn1.st_frame(CGRectMake(10, 10,100, 100)).
             st_font(30).
             st_nomalTitle(@"good").
             st_nomalTitleColor([UIColor redColor]).
             st_nomalImage(@"compose_add_background").
             st_nomalBackgroundImage(@"new_feature_finish_button");

功能3：设置label的frame，title，textColor，font，backgroundColor，textAlignment（因没有提示，textAlignment属性建议使用系统方法设置）

          例：
                 UILabel *label = [[UILabel alloc]init];
                 label.st_frame(CGRectMake(120, 120, 100, 100)).
                 st_title(@"haha").
                 st_textColor([UIColor whiteColor]).
                 st_font(25).
                 st_backgroundColor([UIColor blueColor]).
                 st_textAlignment(NSTextAlignmentCenter);
                 [self.view addSubview:label];

 功能四：设置view的frame及backgroundColor

           例：
                UIView *view = [[UIView alloc]init];
                view.st_backgroundColor([UIColor yellowColor]).
                st_frame(CGRectMake(220, 220, 100, 100));
                [self.view addSubview:view];

功能五： 设置ImageView的frame，backgroundColor，image

              UIImageView *imageView = [[UIImageView alloc]init];
              imageView.st_frame(CGRectMake(200, 400, 150, 150)).
              st_backgroundColor([UIColor grayColor]).
              st_image(@"common_icon_membership_level3");
              [self.view addSubview:imageView];


                            使用说明：

       1.将分类放入项目中、导入头文件并编译，即可使用。
       2.修改frame值直接可以用点语法点出(例：view.x)
       3.设置控件的属性，以“st_”开头，选择要设置的属性即可。如果是button分状态设置，在"st_"后加上状态即可（例：st_nomal****）
      


