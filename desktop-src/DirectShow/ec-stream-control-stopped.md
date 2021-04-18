---
description: Um comando de parada de controle de fluxo teve efeito.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760094"
---
# <a name="ec_stream_control_stopped"></a>controle de fluxo do EC \_ \_ \_ interrompido

Um comando de parada de controle de fluxo teve efeito.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN que interrompeu o fluxo.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valor definido pelo usuário.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

Os filtros enviam esse evento em resposta ao método [**IAMStreamControl:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . O método **STOPAT** especifica um tempo de referência para um PIN parar de transmitir. Quando o streaming é interrompido, o filtro envia esse evento.

O parâmetro *pSender* especifica o PIN que executa o comando Stop. Dependendo da implementação, pode não ser o PIN que recebeu a chamada [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

O parâmetro *dwCookie* é especificado pelo aplicativo no método [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . Esse parâmetro permite que o aplicativo rastreie várias chamadas para o método.

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

 

 




