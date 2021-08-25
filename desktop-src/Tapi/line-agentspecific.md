---
description: A mensagem TAPI LINE AGENTSPECIFIC é enviada quando o status de um agente ACD muda em uma linha que o \_ aplicativo tem aberto no momento. O aplicativo pode invocar lineGetAgentStatus para determinar o status atual do agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: LINE_AGENTSPECIFIC mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87b0e6f5c6c96842f70ebe46c0b72e33e6767c996fa2cc5b4d8e95ff0f08cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867156"
---
# <a name="line_agentspecific-message"></a>Mensagem LINE \_ AGENTSPECIFIC

A mensagem TAPI **LINE \_ AGENTSPECIFIC** é enviada quando o status de um agente ACD muda em uma linha que o aplicativo tem aberto no momento. O aplicativo pode invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar o status atual do agente.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

O alça do aplicativo para o dispositivo de linha.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha da chamada.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

O índice na matriz de identificadores de extensão do manipulador na estrutura [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) da extensão do manipulador à qual a mensagem está associada.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Específico para a extensão do manipulador. Geralmente, esse valor é usado para fazer com que o aplicativo invoque uma [**função lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) para buscar mais detalhes sobre a mensagem.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico para a extensão do manipulador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem LINE \_ AGENTSPECIFIC** não é enviada a aplicativos que suportam versões mais antigas do TAPI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




