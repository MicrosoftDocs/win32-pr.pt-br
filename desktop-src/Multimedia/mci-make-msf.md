---
title: MCI_MAKE_MSF macro (Mciapi.h)
description: A macro MCI MAKE MSF cria um valor temporal no formato \_ MSF (minutos/segundos/quadros) empacotados com base nos valores de minutos, segundos e \_ quadros determinados.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF macro Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f5cfa2b99f7bdbd7eb3029b3f0186904d8b8e94f455614464fadc98cdd20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690125"
---
# <a name="mci_make_msf-macro"></a>Macro MCI \_ MAKE \_ MSF

A macro **MCI \_ MAKE \_ MSF** cria um valor temporal no formato MSF (minutos/segundos/quadros) empacotados com base nos valores de minutos, segundos e quadros determinados.

## <a name="syntax"></a>Sintaxe


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*minutos* 
</dt> <dd>

Número de minutos.

</dd> <dt>

*segundos* 
</dt> <dd>

Número de segundos.

</dd> <dt>

*molduras* 
</dt> <dd>

Número de quadros.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a hora no formato MSF empacotado.

## <a name="remarks"></a>Comentários

O tempo no formato MSF é expresso como um valor **DWORD** com o byte menos significativo contendo minutos, o próximo byte menos significativo contendo segundos e o próximo byte menos significativo contendo quadros. O byte mais significativo não éusado.

A **macro MCI \_ MAKE \_ MSF** é definida da seguinte forma:


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
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

 

 





