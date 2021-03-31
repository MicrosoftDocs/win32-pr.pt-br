---
title: Macro MCI_TMSF_FRAME (Mciapi. h)
description: A \_ macro do quadro MCI TMSF \_ recupera o componente de quadros de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- Multimídia MCI_TMSF_FRAME macro do Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644338"
---
# <a name="mci_tmsf_frame-macro"></a>\_Macro do \_ quadro MCI TMSF

A macro do **\_ \_ quadro MCI TMSF** recupera o componente de quadros de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_TMSF_FRAME(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwTMSF* 
</dt> <dd>

Hora no formato TMSF.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o componente de quadros das informações de TMSF especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.

A macro do **\_ \_ quadro MCI TMSF** é definida da seguinte maneira:


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
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

 

 





