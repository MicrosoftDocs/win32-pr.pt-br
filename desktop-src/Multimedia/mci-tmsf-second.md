---
title: Macro MCI_TMSF_SECOND (Mciapi. h)
description: A \_ segunda macro do MCI TMSF \_ recupera o componente de segundos de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- Multimídia MCI_TMSF_SECOND macro do Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722949487400f80ed72f9e120d5dbf8678ab81a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085665"
---
# <a name="mci_tmsf_second-macro"></a>\_Macro da \_ segunda TMSF MCI

A **\_ \_ segunda macro do MCI TMSF** recupera o componente de segundos de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_TMSF_SECOND(
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

Retorna o componente de segundos das informações de TMSF especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.

A **\_ \_ segunda macro TMSF do MCI** é definida da seguinte maneira:


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
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

 

 





