---
title: Macro MCI_HMS_SECOND (Mciapi. h)
description: A \_ segunda macro do MCI HMS \_ recupera o componente de segundos de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- Multimídia MCI_HMS_SECOND macro do Windows
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824787"
---
# <a name="mci_hms_second-macro"></a>\_Macro da \_ segunda HMS MCI

A **\_ \_ segunda macro do MCI HMS** recupera o componente de segundos de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_HMS_SECOND(
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

Retorna o componente de segundos das informações de HMS especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo que contém minutos e o próximo byte menos significativo que contém segundos. O byte mais significativo não é usado.

A **\_ \_ segunda macro HMS do MCI** é definida da seguinte maneira:


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
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

 

 





