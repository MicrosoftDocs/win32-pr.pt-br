---
description: O método GetEventData aloca espaço para as estruturas NMEVENTDATA e NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: Método IMonitorEventer::GetEventData (Netmon.h)
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
ms.openlocfilehash: 3a089e57ac5f66187f97dfa6ae7533aeda620632bdbf35c7b5bf3a34d4654b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037366"
---
# <a name="imonitoreventergeteventdata-method"></a>Método IMonitorEventer::GetEventData

O **método GetEventData** aloca espaço para as estruturas [NMEVENTDATA](nmeventdata.md) [e NMCOLUMNINFO.](nmcolumninfo.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bNumColumns* \[ Em\]
</dt> <dd>

Número de **estruturas NMCOLUMNINFO** necessárias.

</dd> <dt>

*ppNMEventData* \[ out\]
</dt> <dd>

Endereço da estrutura **NMEVENTDATA** retornada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será S \_ OK.

Se o método não for bem-sucedido, o valor de retorno será NMERR \_ OUT \_ OF \_ MEMORY.

## <a name="remarks"></a>Comentários

Os monitores chamam esse método para alocar memória para os dados de evento e estruturas de informações de coluna. Para liberar memória alocada para uma **estrutura NMEVENTDATA,** consulte [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



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

 

 




