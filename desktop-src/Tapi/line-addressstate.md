---
description: A \_ mensagem de endereço de linha de TAPI é enviada quando o status de um endereço é alterado em uma linha que está aberta no momento pelo aplicativo. O aplicativo pode invocar lineGetAddressStatus para determinar o status atual do endereço.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Mensagem de LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759465"
---
# <a name="line_addressstate-message"></a>\_Mensagem addressstate de linha

A mensagem **de \_ endereço de linha** de TAPI é enviada quando o status de um endereço é alterado em uma linha que está aberta no momento pelo aplicativo. O aplicativo pode invocar [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) para determinar o status atual do endereço.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para o dispositivo de linha.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O identificador de endereço do endereço que alterou o status.

</dd> <dt>

*dwParam2* 
</dt> <dd>

O estado do endereço que foi alterado. Pode ser uma ou mais das [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem \_ Addressstate de linha** é enviada para qualquer aplicativo que tenha aberto o dispositivo de linha e que tenha habilitado esta mensagem. O envio dessa mensagem para os vários itens de status pode ser controlado e consultado usando [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) e [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Por padrão, o relatório de status de endereço é desabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




