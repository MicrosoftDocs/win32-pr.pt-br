---
description: 'Método IEnumMedia:: clone – o método clone cria outro enumerador que contém o mesmo estado de enumeração que o atual.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'Método IEnumMedia:: clone (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894457684e94d07426511979dcb40cfcbbe75ed9fec91e024f09175389261620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992436"
---
# <a name="ienummediaclone-method"></a>Método IEnumMedia:: clone

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **clone** cria outro enumerador que contém o mesmo estado de enumeração que o atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* \[ fora\]
</dt> <dd>

Ponteiro para o novo objeto [**IEnumMedia**](ienummedia.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppEnum* não é um ponteiro válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | Falha por motivos desconhecidos.<br/>                          |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método **AddRef** na interface [**IEnumMedia**](ienummedia.md) retornada por **IEnumMedia:: clone**. O aplicativo deve chamar **Release** na interface **IEnumMedia** para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




