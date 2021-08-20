---
description: Gerenciamento de eras para o calendário japonês
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Gerenciamento de eras para o calendário japonês
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6ba9c8957bc37a3e200aad546d04629b049dfb3a7962f73d463358d879fb718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949415"
---
# <a name="era-handling-for-the-japanese-calendar"></a>Gerenciamento de eras para o calendário japonês

Muitos calendários têm apagamento, como AD/BC ou CE/A.C.. No calendário do japonês, os anos são descritos por nengō, uma combinação do número do ano e do nome da era. Por exemplo, 2009 é Heisei 21. No passado, os nomes de era japoneses mudaram com frequência, mas agora o apagamento em Japonês é alterado apenas em sucessão Imperial. Windows e Microsoft .NET têm suporte historicamente os quatro apagamentos modernos sob esta política: Meiji, Taishō, Shōwa e Heisei.

com o Windows 7, Windows Server 2008 R2 e o .NET Framework 4, a Microsoft reconhece que o apagamento adicional pode ser adicionado no futuro. nessas versões do Windows os dados da era são armazenados no registro sob a chave:<dl> HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ NLS \\ calendários \\ Japonês \\ apagar  
</dl>

se necessário, o apagamento adicional pode ser adicionado a essa chave por meio do processo normal de Windows Update. Essa chave pode ser exibida usando o editor do registro (Regedit.exe). um exemplo da chave e dos valores enviados no Windows 7 é:

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

O nome de cada valor de era a data em que a era começa no calendário gregoriano. O valor contém o nome da era em Japonês, o nome abreviado em Japonês, o nome em inglês e um nome abreviado em inglês:<dl> "aaaa MM DD" = "JE \_ AJE \_ EE \_ AEE"  
</dl>where

-   "Aaaa MM DD" é a data do calendário gregoriano do início da era no formato de ano, mês, dia em que o ano é de 4 dígitos, o dia é 2 dígitos e o mês também tem 2 dígitos. Um espaço separa cada parte da data.
-   "JE" é o nome japonês da era e é seguido por um sublinhado.
-   "AJE" é o nome abreviado da era, em Japonês, e é seguido por um sublinhado.
-   "EE" é o nome em inglês da era japonesa e é seguido por um sublinhado.
-   "AEE" é o nome abreviado em inglês da era japonesa.

uma consideração para os desenvolvedores de aplicativos é a possibilidade de que o apagamento adicional seja adicionado por Windows Update ou outros meios. Nesse caso, o aplicativo pode encontrar mais do que os quatro apagados esperados para o calendário japonês. Para testadores de fins de teste podem adicionar uma era adicional ao registro; no entanto, isso deve ser restrito apenas a computadores de teste, pois ele afeta o comportamento de todo o computador.

Um exemplo de tal chave que poderia ser usada para o teste a seguir. Essa alteração pode ser feita com o editor do registro. (Este é um exemplo de uso de teste somente e não pretende prever quaisquer adições futuras.)

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

observe que isso afeta apenas os computadores que executam o Windows 7 e posterior ou .NET Framework 4 e posterior. Os desenvolvedores de aplicativos são incentivados a testar seus aplicativos com tal teste adicional de apagamento para garantir que seus aplicativos continuem a funcionar se o apagamento adicional for adicionado em alguma data futura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recuperando informações de data e hora](retrieving-time-and-date-information.md)
</dt> <dt>

[Identificadores de calendário](calendar-identifiers.md)
</dt> </dl>

 

 



