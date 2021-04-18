---
description: A \_ mensagem de AGENTSTATUS de linha TAPI é enviada quando o status de um agente AD é alterado em uma linha que o aplicativo abriu no momento. O aplicativo pode invocar lineGetAgentStatus para determinar o status atual do agente.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Mensagem de LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789454"
---
# <a name="line_agentstatus-message"></a>Mensagem de AGENTSTATUS de linha \_

A mensagem **de \_ AGENTSTATUS de linha** TAPI é enviada quando o status de um agente AD é alterado em uma linha que o aplicativo abriu no momento. O aplicativo pode invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar o status atual do agente.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

O identificador do aplicativo para o dispositivo de linha no qual o status do agente foi alterado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha do telefonema.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador do endereço na linha na qual o status do agente foi alterado. Um identificador de endereço é permanentemente associado a um endereço; o identificador permanece constante nas atualizações do sistema operacional.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica o status do agente que foi alterado; pode ser uma combinação de [**\_ constantes LINEAGENTSTATUS**](lineagentstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam2* incluir o \_ bit de estado LINEAGENTSTATUS, *dwParam3* indicará o novo valor do membro **dwState** em [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus). Caso contrário, esse parâmetro será definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem \_ AGENTSTATUS de linha** não é enviada para aplicativos que dão suporte a versões mais antigas da TAPI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




