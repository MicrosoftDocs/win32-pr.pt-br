---
description: A mensagem de CALLINFO de linha TAPI \_ é enviada quando as informações de chamada sobre a chamada especificada foram alteradas. O aplicativo pode invocar lineGetCallInfo para determinar as informações de chamada atuais.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Mensagem de LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792620"
---
# <a name="line_callinfo-message"></a>Mensagem de CALLINFO de linha \_

A mensagem **de \_ CALLINFO de linha** TAPI é enviada quando as informações de chamada sobre a chamada especificada foram alteradas. O aplicativo pode invocar [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para determinar as informações de chamada atuais.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para a chamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha do telefonema.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O item de informações de chamada que foi alterado. Pode ser uma ou mais das [**\_ constantes LINECALLINFOSTATE**](linecallinfostate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Uma mensagem de **\_ CALLINFO de linha** com uma indicação *NumOwnersIncr*, *NumOwnersDecr* e/ou *NumMonitorsChanged* é enviada para aplicativos que já têm um identificador para a chamada. Isso pode ser o resultado de outro aplicativo que altera a propriedade ou monitoração para uma chamada com [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)e [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).

Essas mensagens de **\_ CALLINFO de linha** não são enviadas quando uma notificação de uma nova chamada é fornecida em uma mensagem [**\_ callstate de linha**](line-callstate.md) , porque as informações de chamada já refletem o número correto de proprietários e monitores no momento em que as \_ mensagens callstate de linha são enviadas. **Linha \_** As mensagens CALLINFO também são suprimidas no caso em que uma chamada é oferecida pela TAPI para monitorar por meio do \_ mecanismo desconhecido de LINECALLSTATE.

> [!Note]  
> O aplicativo que faz uma alteração no número de proprietários ou monitores (por exemplo, invocando [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) ou [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) não recebe uma mensagem indicando que a alteração foi feita.

 

Nenhuma mensagem de **\_ CALLINFO de linha** é enviada para uma chamada depois que a chamada entrou no estado *ocioso* . Especificamente, as alterações no número de proprietários e monitores não são relatadas à medida que os aplicativos desalocam seus identificadores para a chamada ociosa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




