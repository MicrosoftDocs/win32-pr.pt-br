---
description: O modo de exibição foi alterado.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee75517c1927d7f819565d796d9f15fb21050ef7b4ead86d98f582018cc66b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965916"
---
# <a name="ec_display_changed"></a>exibição do EC \_ \_ alterada

O modo de exibição foi alterado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para uma matriz de interfaces [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) para os Pins de entrada do processador de vídeo. Se *lParam2* for zero, esse parâmetro poderá ser **nulo**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Se *lParam2* for zero, *lParam1* conterá um único ponteiro **IPin** ou será igual a **NULL**. Se *lParam2* for maior que zero, *lParam1* conterá uma matriz de ponteiros **IPin** e o número de elementos na matriz será fornecido por *lParam2*.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O Gerenciador do grafo de filtro interrompe temporariamente o grafo e, em seguida, desconecta e reconecta o processador de vídeo. Ele não passa o evento para o aplicativo.

## <a name="remarks"></a>Comentários

Os renderizadores de vídeo podem enviar esse evento em resposta a uma mensagem do [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) . A mensagem do **WM \_ DISPLAYCHANGE** indica que o usuário alterou a resolução de vídeo.

Durante a conexão do PIN, a maioria dos renderizadores de vídeo escolhe um formato com base no modo de exibição atual. Se o modo de exibição for alterado, o processador de vídeo poderá precisar escolher outro formato. Ao enviar essa mensagem, o renderizador sinaliza para o Gerenciador do grafo de filtro que precisa ser reconectado. Durante a reconexão, o renderizador pode selecionar um novo formato. Se a reconexão falhar, o Gerenciador do grafo de filtro enviará um evento [**\_ ERRORABORT do EC**](ec-errorabort.md) para o aplicativo.

### <a name="enhanced-video-renderer"></a>Processador de vídeo aprimorado

Um apresentador personalizado para o [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR) deve enviar esse evento para o EVR se o dispositivo Direct3D do apresentador for alterado. Definir *lParam1* e *lParam2* como zero; o EVR ignora os parâmetros de evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

