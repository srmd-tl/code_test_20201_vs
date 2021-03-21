-First of all i consider this code as below OK. The main thing that i prefer is strict typing.So, you guys are not using strict typing and no return type which i think is bad.
-Secondly i see  unused local variables. On line 471 and 720 of BookingRepository , we can make it inline as following
return User::getPotentialUsers($translator_type, $joblanguage, $gender, $translator_level, $translatorsId);
return TeHelper::convertJobIdsInObjs($job_ids);
-PhpDoc Blocks are poorly created.(some of them are missing @return , some are not using proper imports and some of the functions are even missing whole PhpDoc Bloc)
-In some of the functions the statement is not even reachable, for example on line # 199 of BookingRepository,throw statement is being used after return statement. Which makes it unreachable
-Optional parameters are supposed to placed after the required params.In this code its opposite
-params types are not compatible
