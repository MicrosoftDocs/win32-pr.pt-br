---
description: A mensagem de solicitação de linha TAPI \_ é enviada para relatar a chegada de uma nova solicitação de outro aplicativo.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Mensagem de LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cd49b14aafabfdd4d7ab37c5f2beec1487a08a53385ae8a1439b7443d49cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126226"
---
# <a name="line_request-message"></a>Mensagem de solicitação de linha \_

A mensagem **de \_ solicitação de linha** TAPI é enviada para relatar a chegada de uma nova solicitação de outro aplicativo.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de registro do aplicativo especificado em [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).

</dd> <dt>

*dwParam1* 
</dt> <dd>

O modo de solicitação da solicitação recentemente pendente. Esse parâmetro usa as [**\_ constantes LINEREQUESTMODE**](linerequestmode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

As condições para esse parâmetro serão, se *dwParam1* for definido como LINEREQUESTMODE \_ drop, *DwParam2* conterá o *HWND* do aplicativo solicitando a remoção. Caso contrário, *dwParam2* não será usado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam1* for definido como LINEREQUESTMODE \_ drop, a palavra de ordem inferior de *dwParam3* conterá *wRequestID* conforme especificado pelo aplicativo que solicitou o descarte. Caso contrário, *dwParam3* não será usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A mensagem de **\_ solicitação de linha** é enviada para o aplicativo de prioridade mais alta que foi registrado para o modo de solicitação correspondente. Essa mensagem indica a chegada de uma solicitação de telefonia assistida do modo de solicitação especificado. Se *dwParam1* for LINEREQUESTMODE \_ MAKECALL, o aplicativo poderá invocar [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) usando o modo de solicitação correspondente para receber a solicitação. Se *dwParam1* for LINEREQUESTMODE \_ drop, a mensagem conterá todos os dados exigidos pelo destinatário da solicitação para executar a solicitação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapiRequestMakeCall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




