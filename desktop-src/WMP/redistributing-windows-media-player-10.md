---
title: Redistribuindo o Windows Media Player 10
description: Redistribuindo o Windows Media Player 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635038"
---
# <a name="redistributing-windows-media-player-10"></a>Redistribuindo o Windows Media Player 10

Você pode instalar o Windows Media Player 10 no Windows XP usando o programa de instalação a seguir.

-   MP10Setup.exe

Aqui está um exemplo de uma linha de comando para instalação sem interface do usuário e nenhum prompt de reinicialização ou reinicialização.


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



A tabela a seguir mostra parâmetros adicionais que você pode usar com o programa de instalação do Windows Media Player 10.



| Parâmetro              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedir a migração da biblioteca.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Crie um ponto de restauração do sistema aninhado. Use esta se o aplicativo criar um ponto de restauração do sistema para aninhar o ponto de restauração do Windows Media Player no ponto de restauração do aplicativo.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Não permitir a criação de um ponto de restauração do sistema. Esse sinalizador desabilitará a criação de um ponto de restauração do sistema. Na maioria das circunstâncias, esse sinalizador não deve ser usado para a redistribuição de software geral. Isso deve ser usado somente quando você pode fazer uma escolha explícita em nome do usuário final para não oferecer suporte à reversão dos arquivos do Windows Media Player para uma versão anterior do Player. Esse sinalizador deve ser usado somente para a implantação corporativa ou para a instalação do OEM (fabricante original do equipamento). |
| /DefaultService        | Defina o repositório online inicial. Para obter mais informações, consulte [parâmetros de linha de comando de instalação para lojas online](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuindo o software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




