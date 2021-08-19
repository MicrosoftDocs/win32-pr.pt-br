---
description: Método IEnumTime::Skip – o método Skip ignora o próximo número especificado de elementos na sequência de enumeração.
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: Método IEnumTime::Skip (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36f92ead711c25b385c2a7109dbb113b8c5ca082fda9c3012204384350a3c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762945"
---
# <a name="ienumtimeskip-method"></a>Método IEnumTime::Skip

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Skip** ignora o próximo número especificado de elementos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ao mesmo tempo* \[ Em\]
</dt> <dd>

Número de elementos a ignorar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                             | Descrição                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | O número de elementos ignorados *foi ignorado.*<br/>     |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | O número de elementos ignorados não *foi ignorado.*<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




