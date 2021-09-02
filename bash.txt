shareOrg() {
    UPLINE=$(tput cuu1)
    ERASELINE=$(tput el)
    echo "\n\n(ヘ･_･)ヘ┳━┳\n\ncopying...\n"
    sfdx force:org:open -u $1 --urlonly | grep -o "https.*" | pbcopy
    echo "$UPLINE$ERASELINE$UPLINE$ERASELINE$UPLINE$ERASELINE$UPLINE$ERASELINE$UPLINE$ERASELINE\c"
    echo "\n(╯°□°）╯︵ ┻━┻\n\nCOPIED!\n"
}
