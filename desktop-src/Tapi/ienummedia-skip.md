---
description: 'Método IEnumMedia:: Skip – o método Skip ignora o próximo número especificado de elementos na sequência de enumeração.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'Método IEnumMedia:: Skip (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8c600a201d6800fcb04dba5f208fd5cb810078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084184"
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

## <a name="return-value"></a>Valor retornado

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




