---
description: A mensagem TAPI LINE ADDRESSSTATE é enviada quando o status de um endereço muda em uma linha que está aberta \_ no momento pelo aplicativo. O aplicativo pode invocar lineGetAddressStatus para determinar o status atual do endereço.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: LINE_ADDRESSSTATE mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfc158bd41b635142252546fbc289ed868851a3ac79d80bddba2df6118715bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959876"
---
# <a name="line_addressstate-message"></a>Mensagem LINE \_ ADDRESSSTATE

A mensagem TAPI **LINE \_ ADDRESSSTATE** é enviada quando o status de um endereço muda em uma linha que está aberta no momento pelo aplicativo. O aplicativo pode invocar [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) para determinar o status atual do endereço.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um alça para o dispositivo de linha.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

O identificador de endereço do endereço que alterou o status.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

O estado do endereço que foi alterado. Pode ser uma ou mais das [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem LINE \_ ADDRESSSTATE** é enviada a qualquer aplicativo que tenha aberto o dispositivo de linha e que tenha habilitado essa mensagem. O envio dessa mensagem para os vários itens de status pode ser controlado e consultado usando [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) e [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Por padrão, o relatório de status de endereço está desabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**Linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**Linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




