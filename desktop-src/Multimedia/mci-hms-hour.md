---
title: Macro MCI_HMS_HOUR (Mciapi. h)
description: A \_ macro HMS de hora do MCI \_ recupera o componente de horas de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- Multimídia MCI_HMS_HOUR macro do Windows
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009747"
---
# <a name="mci_hms_hour-macro"></a>\_Macro de \_ hora HMS MCI

A **macro \_ HMS de \_ hora do MCI** recupera o componente de horas de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_HMS_HOUR(
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

Retorna o componente de horas das informações de HMS especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo que contém minutos e o próximo byte menos significativo que contém segundos. O byte mais significativo não é usado.

A **macro \_ HMS de \_ hora do MCI** é definida da seguinte maneira:


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
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

 

 





