---
title: Macro MCI_HMS_HOUR (Mciapi. h)
description: A \_ macro HMS de hora do MCI \_ recupera o componente de horas de um parâmetro que contém as informações de horas/minutos/segundos (HMS) compactadas.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- macro de MCI_HMS_HOUR Windows multimídia
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
ms.openlocfilehash: 97b8000e642d18f8499be5f8622a1cf7540fefbd041b7d34f23e1fd5e231815a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039266"
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

## <a name="return-value"></a>Valor retornado

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

 

 





