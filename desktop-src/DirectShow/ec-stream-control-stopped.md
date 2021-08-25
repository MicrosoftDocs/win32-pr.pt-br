---
description: Um comando stream-control stop teve efeito.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69884ecc573b2bb775092529cb81e1b33a1514d4799af9f55c7bcebb5ebd2b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928416"
---
# <a name="ec_stream_control_stopped"></a>CONTROLE DE FLUXO DE EC \_ \_ \_ INTERROMPIDO

Um comando stream-control stop teve efeito.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*Psender*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino que interrompeu o fluxo.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*Dwcookie*
</dt> <dd>

(**DWORD**) Valor definido pelo usuário.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

Os filtros enviam esse evento em resposta ao [**método IAMStreamControl::StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) O **método StopAt** especifica um tempo de referência para um pino parar o streaming. Quando o streaming é interrompido, o filtro envia esse evento.

O *parâmetro pSender* especifica o pino que executa o comando stop. Dependendo da implementação, pode não ser o pino que recebeu a [**chamada StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat)

O *parâmetro dwCookie* é especificado pelo aplicativo no [**método StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) Esse parâmetro permite que o aplicativo acompanhe várias chamadas para o método .

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

 

 




