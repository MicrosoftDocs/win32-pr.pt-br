---
title: Redistribuindo o Windows Media Player 11
description: Redistribuindo o Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005292"
---
# <a name="redistributing-windows-media-player-11"></a>Redistribuindo o Windows Media Player 11

Você pode instalar o Windows Media Player 11 no Windows XP usando um dos programas de instalação a seguir, em que *LocaleID* é um identificador de localidade.

-   wmp11-windowsxp-x86-*LocaleID*. exe
-   wmp11-windowsxp-x64-*LocaleID*. exe

Aqui está um exemplo de uma linha de comando para instalação sem interface do usuário e nenhum prompt de reinicialização ou reinicialização.


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



A tabela a seguir mostra parâmetros adicionais que você pode usar com o programa de instalação do Windows Media Player 11.



| Parâmetro              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedir a migração da biblioteca.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Crie um ponto de restauração do sistema aninhado. Use esta se o aplicativo criar um ponto de restauração do sistema para aninhar o ponto de restauração do Windows Media Player no ponto de restauração do aplicativo.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Não permitir a criação de um ponto de restauração do sistema. Esse sinalizador desabilitará a criação de um ponto de restauração do sistema. Na maioria das circunstâncias, esse sinalizador não deve ser usado para a redistribuição de software geral. Isso deve ser usado somente quando você pode fazer uma escolha explícita em nome do usuário final para não oferecer suporte à reversão dos arquivos do Windows Media Player para uma versão anterior do Player. Esse sinalizador deve ser usado somente para a implantação corporativa ou para a instalação do OEM (fabricante original do equipamento). |
| /DefaultService        | Defina o repositório online inicial. Para obter mais informações, consulte [parâmetros de linha de comando de instalação para lojas online](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuindo o software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




