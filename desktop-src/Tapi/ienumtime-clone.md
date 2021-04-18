---
description: O método clone cria outro enumerador que contém o mesmo estado de enumeração que o atual.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'Método IEnumTime:: clone (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778408"
---
# <a name="ienumtimeclone-method"></a>Método IEnumTime:: clone

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **clone** cria outro enumerador que contém o mesmo estado de enumeração que o atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* \[ fora\]
</dt> <dd>

Ponteiro para o novo objeto [**IEnumTime**](ienumtime.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppEnum* não é um ponteiro válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | Falha por motivos desconhecidos.<br/>                          |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método **AddRef** na interface [**IEnumTime**](ienumtime.md) retornada por **IEnumTime:: clone**. O aplicativo deve chamar **Release** na interface **IEnumTime** para liberar recursos associados a ela.

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

 

 




