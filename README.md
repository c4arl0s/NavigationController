# NavigationController

# Creating the Top–Level View Controller

``` objective-c
#import "AppDelegate.h"
#import "BIDFirstLevelViewController.h"

@interface AppDelegate ()

@end

@implementation AppDelegate


- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    
    self.window = [[UIWindow alloc] initWithFrame:[[UIScreen mainScreen] bounds]];
    // override point for customization after application launch.
    BIDFirstLevelViewController *firstLevelViewController = [[BIDFirstLevelViewController alloc] init];
    firstLevelViewController.view.backgroundColor = [UIColor redColor];
    UINavigationController *navigationController = [[UINavigationController alloc] initWithRootViewController:firstLevelViewController];
    self.window.rootViewController = navigationController;
    self.window.backgroundColor = [UIColor redColor];
    [self.window makeKeyAndVisible];
    return YES;
}
```

# AppDelegate

``` objective-c
//
//  AppDelegate.m
//  NavigationControllerByCode
//
//  Created by Carlos Santiago Cruz on 9/16/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import "AppDelegate.h"
#import "BIDFirstLevelViewController.h"

@interface AppDelegate ()

@end

@implementation AppDelegate


- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    
    self.window = [[UIWindow alloc] initWithFrame:[[UIScreen mainScreen] bounds]];
    // override point for customization after application launch.
    BIDFirstLevelViewController *firstLevelViewController = [[BIDFirstLevelViewController alloc] init];
    firstLevelViewController.view.backgroundColor = [UIColor redColor];
    UINavigationController *navigationController = [[UINavigationController alloc] initWithRootViewController:firstLevelViewController];
    self.window.rootViewController = navigationController;
    self.window.backgroundColor = [UIColor redColor];
    [self.window makeKeyAndVisible];
    return YES;
}


- (void)applicationWillResignActive:(UIApplication *)application {
    // Sent when the application is about to move from active to inactive state. This can occur for certain types of temporary interruptions (such as an incoming phone call or SMS message) or when the user quits the application and it begins the transition to the background state.
    // Use this method to pause ongoing tasks, disable timers, and invalidate graphics rendering callbacks. Games should use this method to pause the game.
}


- (void)applicationDidEnterBackground:(UIApplication *)application {
    // Use this method to release shared resources, save user data, invalidate timers, and store enough application state information to restore your application to its current state in case it is terminated later.
    // If your application supports background execution, this method is called instead of applicationWillTerminate: when the user quits.
}


- (void)applicationWillEnterForeground:(UIApplication *)application {
    // Called as part of the transition from the background to the active state; here you can undo many of the changes made on entering the background.
}


- (void)applicationDidBecomeActive:(UIApplication *)application {
    // Restart any tasks that were paused (or not yet started) while the application was inactive. If the application was previously in the background, optionally refresh the user interface.
}


- (void)applicationWillTerminate:(UIApplication *)application {
    // Called when the application is about to terminate. Save data if appropriate. See also applicationDidEnterBackground:.
}


@end
```

![Screen Shot 2019-09-16 at 1 48 07 PM](https://user-images.githubusercontent.com/24994818/64984499-a06a8c80-d888-11e9-9cad-c8eae2dd1c43.png)

