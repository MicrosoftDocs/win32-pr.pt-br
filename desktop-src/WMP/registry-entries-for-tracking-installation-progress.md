---
title: Entradas do Registro para acompanhar o progresso da instalação
description: Entradas do Registro para acompanhar o progresso da instalação
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, acompanhando o progresso da instalação
- Windows Media Player, acompanhamento de progresso da instalação
- Windows Media Player, acompanhamento de progresso de instalações
- Windows Media Player, registro
- registro, acompanhar o progresso da instalação
- registro, acompanhamento de progresso da instalação
- registro, acompanhamento de progresso de instalações
- registry,settings for Windows Media Player
- acompanhar o progresso da instalação
- instalando o acompanhamento de progresso
- acompanhamento de progresso de instalações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7febb9f25a04c5e4358e891f963ab6a8569cfd6facef7e4f2072807bd09e2605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570297"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Entradas do Registro para acompanhar o progresso da instalação

O programa de instalação do Windows Media Player 11,wm.exe, grava as entradas a seguir no Registro para que os programas de instalação possam acompanhar o progresso do programa de instalação do Windows Media Player conforme ele é \_ executado.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



Na sintaxe do Registro anterior, *value é* um espaço reservado para um valor inteiro.

Progress \_ CurrentDialog indica qual caixa de diálogo Windows Media Player configuração está sendo exibida no momento. Progress MaxDialog indica o número total de caixas de diálogo \_ que Windows Mídia será exibida. Por exemplo, se Progress \_ CurrentDialog = 2 e Progress \_ MaxDialog = 5, Windows Media Player está exibindo a segunda caixa de diálogo em uma sequência de cinco.

Progresso \_ CurrentInstall e Progress \_ MaxInstall, juntos, indicam a porcentagem de conclusão da caixa de diálogo atual. Por exemplo, se Progress CurrentInstall = 6 e Progress MaxInstall = 25, a caixa de diálogo atual será \_ \_ 25/6 (ou seja, 24%) concluída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do Registro**](registry-settings.md)
</dt> </dl>

 

 




