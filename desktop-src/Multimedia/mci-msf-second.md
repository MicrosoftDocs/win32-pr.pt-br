---
title: Macro MCI_MSF_SECOND (Mciapi. h)
description: A \_ segunda macro MCI do MSF \_ recupera o componente de segundos de um parâmetro que contém informações de minutos/segundos/quadros compactados (MSF).
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- macro de MCI_MSF_SECOND Windows multimídia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb09643ae8d3ecdf59c6f3631c9dc28f43bba7ee0434ebabed3e4260c3fec01d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138355"
---
# <a name="mci_msf_second-macro"></a>\_Segunda macro do MSF MCI \_

A **\_ \_ segunda macro MCI do MSF** recupera o componente de segundos de um parâmetro que contém informações de minutos/segundos/quadros compactados (MSF).

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwMSF* 
</dt> <dd>

Hora no formato MSF.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o componente de segundos das informações de MSF especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato MSF é expresso como um valor **DWORD** com o byte menos significativo contendo minutos, o próximo byte menos significativo que contém segundos e o próximo byte menos significativo que contém quadros. O byte mais significativo não é usado.

A **\_ \_ segunda macro do MSF MCI** é definida da seguinte maneira:


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
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

 

 





