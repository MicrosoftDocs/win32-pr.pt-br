---
title: MCI_TMSF_SECOND macro (Mciapi.h)
description: A macro MCI TMSF SECOND recupera o componente seconds de um parâmetro que contém informações de \_ \_ faixas/minutos/segundos/quadros/quadros (TMSF).
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND macro Windows Multimídia
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
ms.openlocfilehash: 92dc8f7771df35e9ddc712d263e805ba1e844ca42cde607d7204dc6dc7b350d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784195"
---
# <a name="mci_tmsf_second-macro"></a>Macro MCI \_ TMSF \_ SECOND

A macro **\_ MCI TMSF \_ SECOND** recupera o componente seconds de um parâmetro que contém informações de faixas/minutos/segundos/quadros/quadros (TMSF).

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

## <a name="return-value"></a>Valor retornado

Retorna o componente seconds das informações de TMSF especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo que contém faixas, o próximo byte menos significativo contendo minutos, o próximo byte menos significativo contendo segundos e o byte mais significativo contendo quadros.

A **macro \_ MCI TMSF \_ SECOND** é definida da seguinte forma:


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI Macros](mci-macros.md)
</dt> </dl>

 

 





