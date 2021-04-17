---
description: A TAPI envia a \_ mensagem de estado do telefone para um aplicativo sempre que o status de um dispositivo de telefone é alterado.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Mensagem de PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755176"
---
# <a name="phone_state-message"></a>Mensagem de estado do telefone \_

A TAPI envia a mensagem de **\_ estado do telefone** para um aplicativo sempre que o status de um dispositivo de telefone é alterado.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Um identificador para o dispositivo de telefone.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada do aplicativo fornecida ao abrir o dispositivo de telefone.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O estado do telefone que foi alterado. Esse parâmetro usa uma das [**\_ constantes PHONESTATE**](phonestate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Informações dependentes do estado do telefone detalhando a alteração do status. Esse parâmetro não será usado se vários sinalizadores forem definidos em *dwParam1*, pois vários itens de status foram alterados. O aplicativo deve invocar [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) para obter um conjunto completo de informações.

Se *dwParam1* for \_ proprietário de PHONESTATE, *dwParam2* conterá o novo número de proprietários.

Se *dwParam1* for um PHONESTATE \_ monitores, *dwParam2* conterá o novo número de monitores.

Se *dwParam1* for a lâmpada PHONESTATE \_ , *dwParam2* conterá o identificador de botão/lâmpada da lâmpada que foi alterada.

Se *dwParam1* for PHONESTATE \_ Anéismode, *dwParam2* conterá o novo modo de anel.

Se *dwParam1* for fone de telefone \_ , palestrante ou headset, *dwParam2* conterá o novo modo Hookswitch do Dispositivo Hookswitch. Esse parâmetro usa uma das [**\_ constantes PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O envio da mensagem de **\_ estado do telefone** para o aplicativo pode ser controlado e consultado usando [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) e [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages). Por padrão, essa mensagem é desabilitada para todas as alterações de estado, exceto para \_ REinicialização de PHONESTATE, que não pode ser desabilitada. Essa mensagem é enviada para todos os aplicativos que têm um identificador para o telefone, incluindo aqueles que chamaram [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) com o parâmetro *DWPRIVILEGES* definido como PHONEPRIVILEGE \_ Owner ou PHONEPRIVILEGE \_ Monitor.

Uma mensagem de **\_ estado do telefone** com uma indicação de proprietários e/ou monitores é enviada para aplicativos que já têm um identificador para o telefone. Isso pode ser o resultado de outro aplicativo alterar a propriedade ou a monitoração do dispositivo de telefone com [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) ou [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_fechar telefone**](phone-close.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




