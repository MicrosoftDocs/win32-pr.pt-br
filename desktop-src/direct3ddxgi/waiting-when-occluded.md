---
description: Os aplicativos podem aguardar um evento quando a renderização na tela é desnecessária (ou seja, enquanto estão ocluídos).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Aguardando um evento quando a renderização é desnecessária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db1aa4805aa1dde25947ed25c90d14c9f3c2f4c8693d3599f1382937ee0dbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118517869"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>Aguardando um evento quando a renderização é desnecessária

Os aplicativos podem aguardar um evento quando a renderização na tela é desnecessária (ou seja, enquanto estão ocluídos). Quando o Gerenciador de Janelas da Área de Trabalho (DWM) ou um aplicativo é ocluído, nenhuma renderização é necessária e o sistema operacional pode permanecer em estados de energia inferiores por períodos mais longos. Isso economiza energia e estende a vida útil da bateria.

Um aplicativo pode aguardar um evento quando:

-   Todos os monitores estão desligados.
-   A sessão em que o aplicativo é executado está desconectada.
-   O aplicativo é executado em tela inteira exclusivamente em uma única configuração de monitor.
-   O aplicativo é executado em uma área de trabalho diferente da área de trabalho ativa e não tem permissão para renderizar na área de trabalho ativa.

O sistema operacional dispara o evento quando o aplicativo é capaz de renderizar novamente. O evento não é limpo durante uma atualização do driver ou na procissão de TDR (detecção e recuperação de tempo-extra), no entanto, ele é limpo quando o novo adaptador e os monitores ficam ativos.

Se você quiser que seu aplicativo seja notificado sobre alterações de status de oclusão, o aplicativo deverá se registrar para essas alterações. Um aplicativo pode se registrar para ser notificado sobre alterações de status de oclusão por meio de uma mensagem para uma janela ou por meio da sinalização de evento. Para se registrar para receber mensagens de notificação em uma janela sobre alterações de status de oclusão, um aplicativo chama o [**método IDXGIFactory2::RegisterOcclusionStatusWindow.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) Para se registrar para receber uma notificação de alterações de status de oclusão por meio da sinalização de evento, um aplicativo chama o [**método IDXGIFactory2::RegisterOcclusionStatusEvent.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) Ambos os métodos retornam um ponteiro para um valor de chave que o aplicativo pode usar para não fazer o registro da notificação. Para não fazer o registro da notificação, o aplicativo passa esse valor de chave para o [**método IDXGIFactory2::UnregisterOcclusionStatus.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhorias do DXGI 1.2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



