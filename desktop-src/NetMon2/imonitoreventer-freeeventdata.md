---
description: O método FreeEventData libera espaço alocado para a estrutura NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'Método IMonitorEventer:: FreeEventData (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758742"
---
# <a name="imonitoreventerfreeeventdata-method"></a>Método IMonitorEventer:: FreeEventData

O método **FreeEventData** libera espaço alocado para a estrutura [**NMEVENTDATA**](nmeventdata.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNMEventData* \[ no\]
</dt> <dd>

Endereço da estrutura [**NMEVENTDATA**](nmeventdata.md) , a memória do que é liberada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os monitores chamam esse método para liberar a memória que eles alocam para a estrutura de dados de evento. Lembre-se de que, embora o monitor ainda tenha um ponteiro para cadeias de caracteres em uma estrutura [**NMEVENTDATA**](nmeventdata.md) alocada, a memória para essas cadeias de caracteres deve ser liberada antes que o método **FreeEventData** seja chamado.

Para obter mais informações sobre como alocar memória para uma estrutura [**NMEVENTDATA**](nmeventdata.md) , consulte [**IMonitorEventer:: GetEventData**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**NMEVENTDATA**](nmeventdata.md)
</dt> </dl>

 

 




