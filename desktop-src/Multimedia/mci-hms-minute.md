---
title: Macro MCI_HMS_MINUTE (Mciapi. h)
description: A \_ macro HMS \_ minute do MCI recupera o componente de minutos de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- Multimídia MCI_HMS_MINUTE macro do Windows
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086399"
---
# <a name="mci_hms_minute-macro"></a>\_Macro de \_ minuto HMS MCI

A **macro \_ HMS \_ minute do MCI** recupera o componente de minutos de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwHMS* 
</dt> <dd>

Hora no formato HMS.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o componente de minutos das informações de HMS especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo que contém minutos e o próximo byte menos significativo que contém segundos. O byte mais significativo não é usado.

A macro **MCI \_ HMS \_ minute** é definida da seguinte maneira:


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Macros MCI](mci-macros.md)
</dt> </dl>

 

 





