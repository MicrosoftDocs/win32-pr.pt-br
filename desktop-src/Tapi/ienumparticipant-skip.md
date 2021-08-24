---
description: O método Skip ignora o próximo número especificado de elementos na sequência de enumeração. Esse método está oculto de linguagens Visual Basic script e de script.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: Método IEnumParticipant::Skip (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a55eb3298578738bb427efd6ab2b830b9a7850668aa3c9fa4712cc1bf48d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660696"
---
# <a name="ienumparticipantskip-method"></a>Método IEnumParticipant::Skip

\[**Skip** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Skip** ignora o próximo número especificado de elementos na sequência de enumeração. Esse método está oculto de linguagens Visual Basic script e de script.

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



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O número de elementos ignorados *foi ignorado.*<br/>               |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | O número de elementos ignorados não *foi ignorado.*<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




