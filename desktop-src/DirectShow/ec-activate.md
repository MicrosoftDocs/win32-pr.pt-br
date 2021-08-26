---
description: Uma janela de vídeo está sendo ativada ou desativada.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14d9b0ad192045f179d9f0f366eed6a32efb0e6cc6f61b47255f118b7f55258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966056"
---
# <a name="ec_activate"></a>EC \_ ACTIVATE

Uma janela de vídeo está sendo ativada ou desativada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**BOOL**) **TRUE** se a janela estiver ativada ou **FALSE** se a janela for desativada.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do renderdor.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O gerenciador de grafo de filtro define o foco por meio da interface [**IResourceManager.**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) Ele não envia a notificação de evento para o aplicativo.

## <a name="remarks"></a>Comentários

Um renderador de vídeo envia esse evento sempre que sua janela é ativada ou desativada (ou seja, quando recebe uma mensagem WM \_ ACTIVATEAPP). A ativação ou desativação da janela pode ocorrer porque a janela ganhou ou perdeu o foco ou porque o renderador alternou entre o modo de tela inteira e o modo de janela.

Esse evento permite que o gerenciador de grafo de filtro aloce recursos que dependem do foco da janela, como dispositivos de áudio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




