---
title: Suporte a Unicode para controles comuns
description: Este tópico descreve como dar suporte a Unicode para notificações de controle comuns.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01ab987516f1a91b47f8e5fd5f031631956d8c7bf59cd164edd83d414d5e72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668888"
---
# <a name="unicode-support-for-common-controls"></a>Suporte a Unicode para controles comuns

Este tópico descreve como dar suporte a Unicode para notificações de controle comuns.


para as versões 5,80 e posteriores do comctl32.dll, as notificações de controles comuns dão suporte a formatos ANSI e Unicode em sistemas Windows 95 ou posterior. O sistema determina qual formato usar enviando a janela uma mensagem do [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) . Para especificar um formato, retorne o NFR \_ ANSI para notificações ANSI ou o NFR \_ Unicode para notificações Unicode. Se você não tratar essa mensagem, o sistema chamará [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) para determinar o formato. como Windows 95 e Windows 98 sempre retornam **FALSE** para essa chamada de função, eles usam notificações ANSI por padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles comuns](common-controls-intro.md)
</dt> </dl>

 

 