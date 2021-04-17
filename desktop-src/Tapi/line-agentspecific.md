---
description: A \_ mensagem de AGENTSPECIFIC de linha TAPI é enviada quando o status de um agente AD é alterado em uma linha que o aplicativo abriu no momento. O aplicativo pode invocar lineGetAgentStatus para determinar o status atual do agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Mensagem de LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757209"
---
# <a name="line_agentspecific-message"></a>Mensagem de AGENTSPECIFIC de linha \_

A mensagem **de \_ AGENTSPECIFIC de linha** TAPI é enviada quando o status de um agente AD é alterado em uma linha que o aplicativo abriu no momento. O aplicativo pode invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar o status atual do agente.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

O identificador do aplicativo para o dispositivo de linha.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha do telefonema.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O índice na matriz de identificadores de extensão do manipulador na estrutura [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) da extensão do manipulador à qual a mensagem está associada.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico da extensão do manipulador. Em geral, esse valor é usado para fazer com que o aplicativo invoque uma função [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) para buscar mais detalhes sobre a mensagem.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico da extensão do manipulador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem \_ AGENTSPECIFIC de linha** não é enviada para aplicativos que dão suporte a versões mais antigas da TAPI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




