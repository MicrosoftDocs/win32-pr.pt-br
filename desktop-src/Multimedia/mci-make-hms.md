---
title: Macro MCI_MAKE_HMS (Mciapi. h)
description: O MCI \_ Make \_ HMS macro cria um valor de tempo no formato de horas/minutos/segundos (HMS) empacotado dos valores de horas, minutos e segundos fornecidos.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- Multimídia MCI_MAKE_HMS macro do Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645060"
---
# <a name="mci_make_hms-macro"></a>\_Macro Make \_ HMS do MCI

O **MCI \_ Make \_ HMS** macro cria um valor de tempo no formato de horas/minutos/segundos (HMS) empacotado dos valores de horas, minutos e segundos fornecidos.

## <a name="syntax"></a>Sintaxe


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*duração* 
</dt> <dd>

Número de horas.

</dd> <dt>

*alguns* 
</dt> <dd>

Número de minutos.

</dd> <dt>

*segundos* 
</dt> <dd>

Número de segundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o tempo no formato HMS empacotado.

## <a name="remarks"></a>Comentários

O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo que contém minutos e o próximo byte menos significativo que contém segundos. O byte mais significativo não é usado.

A **macro \_ Make \_ HMS do MCI** é definida da seguinte maneira:


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
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

 

 





