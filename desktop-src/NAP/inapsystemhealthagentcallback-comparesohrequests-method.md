---
title: Método INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent. h)
description: É usado pelo SHA para comparar solicitações SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Método CompareSoHRequests NAP
- Método CompareSoHRequests NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método CompareSoHRequests
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af26786c8ef021794876d8876ae5d8faee65b8cbbfc39b434b000ff502c64c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939431"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>Método INapSystemHealthAgentCallback:: CompareSoHRequests

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentCallback:: CompareSoHRequests** é usado pelo Sha para comparar as solicitações soh.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LHS* \[ no\]
</dt> <dd>

Um ponteiro para o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à esquerda da operação de comparação.

</dd> <dt>

*RHS* \[ no\]
</dt> <dd>

Um ponteiro para o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à direita da operação de comparação.

</dd> <dt>

*IsEqual* \[ fora\]
</dt> <dd>

Um ponteiro para um **bool** que é **verdadeiro** se *LHS* e *RHS* são semanticamente iguais e **false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                               | Description                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Indica êxito.<br/>                         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | O método não foi implementado pelo SHA.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.

O SHA deve comparar o SoHs e retornar **true** se SoHs for semanticamente igual. O NapAgent usa essas informações para determinar se uma troca de SoH deve ser iniciada devido à alteração do estado do computador cliente.

Se os SHAs tiverem colocado IDs incrementais ou carimbos de data/hora em sua SoH, SoHs poderá ser semanticamente igual (ou seja, eles podem transmitir as mesmas informações de integridade), mas podem ser desiguais por byte. Os SHAs devem implementar essa função para verificar a igualdade semântica de SoHs.

Se os SHAs não tiverem colocado carimbos de data/hora ou IDs em seus SoHs, eles poderão optar por não implementar essa função e retornar e **\_ NOTIMPL**. Nesse caso, o NapAgent executa uma comparação de byte no [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





