---
title: Macro MCI_TMSF_TRACK (Mciapi. h)
description: A \_ macro do controle MCI TMSF \_ recupera o componente trilhas de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- Multimídia MCI_TMSF_TRACK macro do Windows
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824470"
---
# <a name="mci_tmsf_track-macro"></a>\_Macro de \_ controle MCI TMSF

A macro do **\_ \_ controle MCI TMSF** recupera o componente trilhas de um parâmetro que contém informações de roteiros/minutos/segundos/quadros (TMSF) compactados.

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_TMSF_TRACK(
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

Retorna o componente de trilhas das informações de TMSF especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.

A macro do **\_ \_ controle MCI TMSF** é definida da seguinte maneira:


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Macros MCI](mci-macros.md)
</dt> </dl>

 

 





