---
description: O método GetEventData aloca espaço para as estruturas NMEVENTDATA e NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'Método IMonitorEventer:: GetEventData (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164409"
---
# <a name="imonitoreventergeteventdata-method"></a>Método IMonitorEventer:: GetEventData

O método **GetEventData** aloca espaço para as estruturas [NMEVENTDATA](nmeventdata.md) e [NMCOLUMNINFO](nmcolumninfo.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bNumColumns* \[ no\]
</dt> <dd>

Número de estruturas **NMCOLUMNINFO** necessárias.

</dd> <dt>

*ppNMEventData* \[ fora\]
</dt> <dd>

Endereço da estrutura **NMEVENTDATA** que é retornada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será S \_ OK.

Se o método não for bem-sucedido, o valor de retorno será NMERR \_ memória insuficiente \_ \_ .

## <a name="remarks"></a>Comentários

Os monitores chamam esse método para alocar memória para os dados de evento e estruturas de informações de coluna. Para liberar memória alocada para uma estrutura **NMEVENTDATA** , consulte [IMonitorEventer:: FreeEventData](imonitoreventer-freeeventdata.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IMonitorEventer](imonitoreventer.md)
</dt> <dt>

[IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md)
</dt> <dt>

[NMEVENTDATA](nmeventdata.md)
</dt> <dt>

[NMCOLUMNINFO](nmcolumninfo.md)
</dt> </dl>

 

 




