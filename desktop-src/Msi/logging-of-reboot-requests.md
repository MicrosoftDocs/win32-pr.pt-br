---
description: Se a ação InstallValidate detectar a instalação de um arquivo em uso, ela exibirá a caixa de diálogo FilesInUse e registrará as informações a seguir.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Registro em log de solicitações de reinicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506254"
---
# <a name="logging-of-reboot-requests"></a>Registro em log de solicitações de reinicialização

Se a [ação InstallValidate](installvalidate-action.md) detectar a instalação de um arquivo em uso, ela exibirá a [caixa de diálogo FilesInUse](filesinuse-dialog.md) e registrará as informações a seguir.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

Se o instalador detectar que está prestes a substituir um arquivo que está em uso, ele registrará as informações a seguir.

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

O \[ token de nome de arquivo \] pode realmente conter um caminho para um arquivo com uma extensão. RBF. Nesse caso, o arquivo. RBF é, na verdade, o arquivo original registrado pela mensagem 1603 que foi renomeada para o arquivo. RBF. O arquivo em uso é renomeado primeiro com uma extensão. RBF e, em seguida, excluído.

Para obter mais informações sobre por que o instalador está tentando substituir esse arquivo específico, você pode usar a opção de log detalhado. Use o \_ valor Verbose INSTALLLOGMODE em uma chamada para [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) ou use a opção de saída detalhada das opções de [linha de comando](command-line-options.md). Isso registra as informações a seguir.

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

O log incluirá uma mensagem como "o arquivo existente é uma versão inferior" ou "o arquivo existente está corrompido (soma de verificação inválida)"

 

 



