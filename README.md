https://docs.github.com/ru/migrations/importing-source-code/using-github-importer/about-github-importer# 1
for me
  use RPi::UnicornHatHD;
    my $display = RPi::UnicornHatHD->new();
    while (1) { # Mini rave!
            $display->set_all(sprintf '#%06X', int rand(hex 'FFFFFF'));
            for (0 .. 100, reverse 0 .. 100) {
                    $display->brightness($_ / 100);
                    $display->show();
            }
    }
