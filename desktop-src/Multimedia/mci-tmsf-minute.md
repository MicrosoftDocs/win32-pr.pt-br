---
title: Macro MCI_TMSF_MINUTE (Mciapi. h)
description: A \_ macro TMSF \_ minute do MCI recupera o componente de minutos de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.
ms.assetid: 9a972579-240f-4641-b65e-9088f39cdf9e
keywords:
- Multimídia MCI_TMSF_MINUTE macro do Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69a12c2622f3f97f04bdca89389c8ab9be7e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499387"
---
# <a name="mci_tmsf_minute-macro"></a>\_Macro de \_ minuto TMSF MCI

A **macro \_ TMSF \_ minute do MCI** recupera o componente de minutos de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_TMSF_MINUTE(
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

Retorna o componente de minutos das informações de TMSF especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.

A macro **MCI \_ TMSF \_ minute** é definida da seguinte maneira:


```C++
#define MCI_TMSF_MINUTE(tmsf) ((BYTE)(((WORD)(tmsf)) >> 8)) 
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

 

 





