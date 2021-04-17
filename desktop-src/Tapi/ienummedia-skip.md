---
description: O método Skip ignora o próximo número especificado de elementos na sequência de enumeração.
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'Método IEnumMedia:: Skip (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd950fd61ad6f6b2030b03d0d269854f86e3a02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769420"
---
# <a name="ienummediaskip-method"></a>Método IEnumMedia:: Skip

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Skip** ignora o próximo número especificado de elementos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

Número de elementos a serem ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                             | Descrição                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | O número de elementos ignorados foi *celt*.<br/>     |
| <dl> <dt>**\_falso**</dt> </dl> | O número de elementos ignorados não era *celt*.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




