---
title: Entradas de registro para acompanhar o progresso da instalação
description: Entradas de registro para acompanhar o progresso da instalação
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, acompanhando o progresso da instalação
- Windows Media Player, acompanhamento do progresso da instalação
- Windows Media Player, acompanhamento de progresso de instalações
- Windows Media Player, registro
- registro, acompanhamento do progresso da instalação
- registro, acompanhamento do progresso da instalação
- registro, acompanhamento de progresso de instalações
- registro, configurações do Windows Media Player
- acompanhamento do progresso da instalação
- Instalando o rastreamento de progresso
- rastreamento de progresso de instalações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006150"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>Entradas de registro para acompanhar o progresso da instalação

O programa de instalação do Windows Media Player 11,wm.exe de instalação \_ , grava as seguintes entradas no registro para que os programas de instalação possam acompanhar o progresso do programa de instalação do Windows Media Player à medida que ele é executado.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



Na sintaxe de registro anterior, *Value* é um espaço reservado para um valor inteiro.

O progresso \_ CurrentDialog indica qual caixa de diálogo a instalação do Windows Media Player está exibindo no momento. O \_ MaxDialog de progresso indica o número total de caixas de diálogo que o Windows Media exibirá. Por exemplo, se Progress \_ CurrentDialog = 2 e Progress \_ MaxDialog = 5, o Windows Media Player está atualmente exibindo a segunda caixa de diálogo em uma sequência de cinco.

Progresso \_ CurrentInstall e MaxInstall de progresso \_ , em conjunto, indicam a porcentagem de conclusão da caixa de diálogo atual. Por exemplo, se Progress \_ CurrentInstall = 6 e Progress \_ MaxInstall = 25, a caixa de diálogo atual será 6/25 (ou seja, 24%) concluí.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro**](registry-settings.md)
</dt> </dl>

 

 




