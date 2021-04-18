---
description: Uma janela de vídeo está sendo ativada ou desativada.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779543"
---
# <a name="ec_activate"></a>ativação do EC \_

Uma janela de vídeo está sendo ativada ou desativada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Bool**) **True** se a janela for ativada ou **false** se a janela for desativada.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do processador.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O Gerenciador de gráfico de filtro define o foco, por meio da interface [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . Ele não envia a notificação de eventos para o aplicativo.

## <a name="remarks"></a>Comentários

Um processador de vídeo envia esse evento sempre que sua janela é ativada ou desativada (ou seja, quando recebe uma mensagem do WM \_ ACTIVATEAPP). A ativação ou desativação de janela pode ocorrer porque a janela obteve ou perdeu o foco, ou porque o renderizador mudou entre o modo de tela inteira e o modo em janela.

Esse evento permite que o Gerenciador do grafo de filtro aloque recursos que dependem do foco da janela, como dispositivos de áudio.

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

 

 




