---
title: MCI_HMS_SECOND macro (Mciapi.h)
description: A macro MCI HMS SECOND recupera o componente seconds de um parâmetro que contém informações de \_ \_ HORAS/minutos/segundos empacotadas (HMS).
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND macro Windows Multimídia
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
ms.openlocfilehash: bc61747d891d3c91afd5e4cb7f9a16eef44e13eb3de275bbf9575d8a4f584d40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039226"
---
# <a name="mci_hms_second-macro"></a>Macro MCI \_ HMS \_ SECOND

A macro **MCI \_ HMS \_ SECOND** recupera o componente seconds de um parâmetro que contém informações de HORAS/minutos/segundos empacotadas (HMS).

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwEARS* 
</dt> <dd>

Hora no formato HMS.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o componente seconds das informações de HMS especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato HMS é expresso como um valor **DWORD** com o byte menos significativo contendo horas, o próximo byte menos significativo contendo minutos e o próximo byte menos significativo contendo segundos. O byte mais significativo não éusado.

A **macro MCI \_ HMS \_ SECOND** é definida da seguinte forma:


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
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

 

 





