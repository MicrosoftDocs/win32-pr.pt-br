---
description: 'Os aplicativos Direct3D podem ser executados em qualquer um dos dois modos: tela inteira ou janela.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Modo de janela versus Full-Screen janela (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a845c464e6c402c46cc4aff09196ccfde65ad90371187045b0c14c41315a9f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025746"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a>Modo de janela versus Full-Screen janela (Direct3D 9)

Os aplicativos Direct3D podem ser executados em qualquer um dos dois modos: tela inteira ou janela.

O modo de tela inteira significa que a janela em que o aplicativo é executado abrange toda a área de trabalho, ocultando todos os aplicativos em execução (incluindo seu ambiente de desenvolvimento). Jogos normalmente usam o modo de tela inteira por padrão para imergir o usuário no jogo, ocultando todos os aplicativos em execução. Um aplicativo em execução no modo de janela compartilha a área de trabalho com todos os aplicativos em execução. As diferenças de código entre o modo de tela inteira e modo de janela são muito pequenas.

Como um aplicativo em execução no modo de tela inteira assume a tela, depurar o aplicativo requer um monitor separado ou o uso de um depurador remoto. Use a [Ferramenta de Painel de Controle DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) para habilitar a depuração de vários monitores. Uma vantagem de um aplicativo de modo de janela é que você pode percorrer o código em um depurador sem vários monitores ou um depurador remoto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 



