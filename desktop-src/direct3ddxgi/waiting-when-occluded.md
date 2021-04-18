---
description: Os aplicativos podem esperar um evento quando a renderização na tela é desnecessária (ou seja, enquanto eles são obstruído).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Aguardando um evento quando a renderização é desnecessária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789529"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>Aguardando um evento quando a renderização é desnecessária

Os aplicativos podem esperar um evento quando a renderização na tela é desnecessária (ou seja, enquanto eles são obstruído). Quando o Gerenciador de Janelas da Área de Trabalho (DWM) ou um aplicativo é obstruídodo, nenhuma renderização é necessária e o sistema operacional pode permanecer em Estados de energia menores por períodos mais longos. Isso economiza energia e estende a vida útil da bateria.

Um aplicativo pode aguardar um evento quando:

-   Todos os monitores estão desligados.
-   A sessão em que o aplicativo é executado está desconectada.
-   O aplicativo é executado em tela inteira exclusivamente em uma única configuração de monitor.
-   O aplicativo é executado em uma área de trabalho diferente da área de trabalho ativa e não tem permissão para renderizar no desktop ativo.

O sistema operacional dispara o evento quando o aplicativo é capaz de renderizar novamente. O evento não é removido durante uma atualização de driver ou um processo de TDR (detecção de tempo limite e recuperação), no entanto, ele é limpo quando o novo adaptador e os monitores se tornam ativos.

Se você quiser que seu aplicativo seja notificado sobre alterações de status do oclusão, o aplicativo deverá se registrar para essas alterações. Um aplicativo pode ser registrado para ser notificado sobre alterações de status de oclusão por meio de uma mensagem em uma janela ou por meio de sinalização de evento. Para se registrar para receber mensagens de notificação em uma janela sobre alterações de status de oclusão, um aplicativo chama o método [**IDXGIFactory2:: RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) . Para se registrar para receber a notificação de alterações de status de oclusão por meio de sinalização de evento, um aplicativo chama o método [**IDXGIFactory2:: RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) . Os dois métodos retornam um ponteiro para um valor de chave que o aplicativo pode usar para cancelar o registro da notificação. Para cancelar o registro da notificação, o aplicativo passa esse valor de chave para o método [**IDXGIFactory2:: UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimoramentos de DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



