---
description: 'Método IEnumMedia:: Next – o próximo método obtém o próximo número especificado de elementos na sequência de enumeração.'
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'Método IEnumMedia:: Next (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711e9c844c46aab6ca90988d4e456e926716b201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113434"
---
# <a name="ienummedianext-method"></a>Método IEnumMedia:: Next

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O **próximo** método obtém o próximo número especificado de elementos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
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

Ponteiro para a interface [**ITMedia**](itmedia.md) .

</dd> <dt>

*pceltFetched* \[ fora\]
</dt> <dd>

Aponta para o número de elementos realmente fornecidos. Poderá ser **NULL** se *celt* for um.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                     | Significado                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método retornou *celt* número de elementos.<br/>         |
| <dl> <dt>**\_falso**</dt> </dl>   | O número de elementos restantes era menor que *celt*.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | O parâmetro *PVal* não é um ponteiro válido.<br/>       |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método **AddRef** na interface [**ITMedia**](itmedia.md) retornada por **IEnumMedia:: Next**. O aplicativo deve chamar **Release** na interface **ITMedia** para liberar recursos associados a ela.

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

 

 




