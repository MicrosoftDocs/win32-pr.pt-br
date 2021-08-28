---
description: A mensagem TAPI LINE AGENTSTATUS é enviada quando o status de um agente ACD muda em uma linha que o \_ aplicativo tem aberto no momento. O aplicativo pode invocar lineGetAgentStatus para determinar o status atual do agente.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: LINE_AGENTSTATUS mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32335e59352b773f84e8a0725c6fd97de679670cbd237f87c3e629985feb43a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959866"
---
# <a name="line_agentstatus-message"></a>Mensagem LINE \_ AGENTSTATUS

A mensagem TAPI **LINE \_ AGENTSTATUS** é enviada quando o status de um agente ACD muda em uma linha que o aplicativo tem aberto no momento. O aplicativo pode invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar o status atual do agente.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

O handle do aplicativo para o dispositivo de linha no qual o status do agente foi alterado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha da chamada.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

Identificador do endereço na linha na qual o status do agente foi alterado. Um identificador de endereço é associado permanentemente a um endereço; O identificador permanece constante entre as atualizações do sistema operacional.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Especifica o status do agente que foi alterado; pode ser uma combinação de [**\_ constantes LINEAGENTSTATUS**](lineagentstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam2* incluir o bit LINEAGENTSTATUS \_ STATE, *dwParam3* indicará o novo valor do membro **dwState** em [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus). Caso contrário, esse parâmetro será definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem LINE \_ AGENTSTATUS** não é enviada a aplicativos que suportam versões mais antigas do TAPI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




