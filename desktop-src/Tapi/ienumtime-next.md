---
description: O próximo método obtém o próximo número especificado de elementos na sequência de enumeração.
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: 'Método IEnumTime:: Next (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce3d88bc88e808c35ec64f827fd5925ddfe57f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780605"
---
# <a name="ienumtimenext-method"></a>Método IEnumTime:: Next

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O **próximo** método obtém o próximo número especificado de elementos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*PVal* \[ fora\]
</dt> <dd>

Ponteiro para a interface [**ITTime**](ittime.md) .

</dd> <dt>

*pceltFetched* \[ fora\]
</dt> <dd>

Aponta para o número de elementos realmente fornecidos. Poderá ser **NULL** se *celt* for 1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                     | Significado                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método retornou *celt* número de elementos.<br/>         |
| <dl> <dt>**\_falso**</dt> </dl>   | O número de elementos restantes era menor que *celt*.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | O parâmetro *PVal* não é um ponteiro válido.<br/>       |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método **AddRef** na interface [**ITTime**](ittime.md) retornada por **IEnumTime:: Next**. O aplicativo deve chamar **Release** na interface **ITTime** para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




