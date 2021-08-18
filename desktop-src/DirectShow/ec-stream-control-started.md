---
description: Um comando de início de controle de fluxo entrou em vigor.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73af8d39c3dae0447600a23dcb00483f4e0da6b81bc7ba6ab4a7e8b5f7afa42d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997886"
---
# <a name="ec_stream_control_started"></a>controle de fluxo de EC \_ \_ \_ iniciado

Um comando de início de controle de fluxo entrou em vigor.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN que iniciou o fluxo.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valor definido pelo usuário.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

Os filtros enviam esse evento em resposta ao método [**IAMStreamControl:: StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Esse método especifica um tempo de referência para um PIN iniciar streaming. Quando o streaming começa, o filtro envia esse evento.

O parâmetro *pSender* especifica o PIN que executa o comando Start. Dependendo da implementação, pode não ser o PIN que recebeu a chamada [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

O parâmetro *dwCookie* é especificado pelo aplicativo no método [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Esse parâmetro permite que o aplicativo rastreie várias chamadas para o método.

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

 

 




