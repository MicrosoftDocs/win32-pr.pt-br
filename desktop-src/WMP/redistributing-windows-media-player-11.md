---
title: Redistribuindo Windows Media Player 11
description: Redistribuindo Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec17042165ed891370d1543fad303150c4b21d1f1db7f9da38de9f75d02876a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746555"
---
# <a name="redistributing-windows-media-player-11"></a>Redistribuindo Windows Media Player 11

Você pode instalar Windows Media Player 11 no Windows XP usando um dos programas de instalação a seguir, em que *localeId* é um identificador de localidade.

-   wmp11-windowsxp-x86-*localeId*.exe
-   wmp11-windowsxp-x64-*localeId*.exe

Aqui está um exemplo de uma linha de comando para instalação sem interface do usuário e sem prompt de reinicialização ou reinicialização.


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



A tabela a seguir mostra parâmetros adicionais que você pode usar com o programa de Windows Media Player 11.



| Parâmetro              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedir a migração de biblioteca.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Crie um ponto de restauração aninhado do sistema. Use isso se o aplicativo criar um ponto de restauração do sistema para aninhar o ponto Windows Media Player restauração dentro do ponto de restauração do aplicativo.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Não permitir a criação de um ponto de restauração do sistema. Esse sinalizador desabilitará a criação de um ponto de restauração do sistema. Na maioria das circunstâncias, esse sinalizador não deve ser usado para redistribuição geral de software. Isso deve ser usado somente quando você puder fazer uma escolha explícita em nome do usuário final para não dar suporte à reversões dos arquivos Windows Media Player para uma versão anterior do Player. Esse sinalizador deve ser usado somente para implantação corporativa ou instalação do OEM (fabricante de equipamento original). |
| /DefaultService        | Definir a loja online inicial. Para obter mais informações, consulte [Configurar parâmetros de linha de comando para lojas online.](setup-command-line-parameters-for-online-stores.md)                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuindo Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




