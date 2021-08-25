---
description: A mensagem de APPNEWCALL de linha TAPI \_ é enviada para informar um aplicativo quando um novo identificador de chamada foi criado espontaneamente em seu nome.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Mensagem de LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22efd93febad5e0199f2ff8897841fe57e8e637acfb8f9cd316386ed913876c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867126"
---
# <a name="line_appnewcall-message"></a>Mensagem de APPNEWCALL de linha \_

A mensagem **de \_ APPNEWCALL de linha** TAPI é enviada para informar um aplicativo quando um novo identificador de chamada foi criado espontaneamente em seu nome (diferente de por meio de uma chamada à API do aplicativo; nesse caso, o identificador teria sido retornado por meio de um parâmetro de ponteiro passado para a função).


```C++
        
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

O identificador do aplicativo para o dispositivo de linha no qual a chamada foi criada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha do telefonema.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador do endereço na linha na qual a chamada é exibida. Um identificador de endereço é permanentemente associado a um endereço; o identificador permanece constante nas atualizações do sistema operacional.

</dd> <dt>

*dwParam2* 
</dt> <dd>

O identificador do aplicativo para a nova chamada.

</dd> <dt>

*dwParam3* 
</dt> <dd>

O privilégio de aplicativos para a nova chamada (LINECALLPRIVILEGE \_ Owner ou LINECALLPRIVILEGE \_ Monitor).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os aplicativos que dão suporte à TAPI versão 2,0 ou posterior são enviados uma mensagem de **linha \_ APPNEWCALL** sempre que o aplicativo recebe espontaneamente um identificador para uma nova chamada. Como a mensagem inclui os parâmetros *hLine* e *dwAddressID* nos quais a chamada existe, o aplicativo pode rapidamente criar um novo objeto de chamada no contexto correto. A **mensagem \_ APPNEWCALL de linha** é sempre imediatamente seguida por uma mensagem [**\_ callstate de linha**](line-callstate.md) que indica o estado inicial da chamada.

Os aplicativos mais antigos (que negociaram uma versão de API anterior a 2,0) são enviados apenas a uma mensagem [**\_ callstate de linha**](line-callstate.md) , conforme documentado em versões anteriores da API. Tais aplicativos criaria um novo objeto de chamada ao receber uma mensagem [**\_ callstate de linha**](line-callstate.md) que tem *dwParam3* definido como um valor diferente de zero e contendo um identificador de chamada não atualmente conhecido pelo aplicativo. As desvantagens são que (a) o aplicativo deve chamar [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para determinar os parâmetros *hLine* e *dwAddressID* associados à chamada; (b) o aplicativo deve verificar todos os identificadores de chamada conhecidos para determinar se a chamada é uma nova chamada; e (c) é possível, em determinadas condições, para o aplicativo acreditar que está recebendo um novo identificador de chamada quando, na realidade, ele apenas desalocou seu identificador para a chamada (por exemplo, o aplicativo acabou de desalocar um identificador de chamada, mas uma mensagem [**\_ callstate de linha**](line-callstate.md) que fornece a propriedade do aplicativo da chamada devido a um [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) de outro aplicativo já estava na fila de mensagens TAPI do aplicativo).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**chamada de LINHAstate \_**](line-callstate.md)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




