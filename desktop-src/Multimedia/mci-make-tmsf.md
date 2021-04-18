---
title: Macro MCI_MAKE_TMSF (Mciapi. h)
description: O MCI \_ Make \_ TMSF macro cria um valor de tempo no formato de faixas/minutos/segundos/quadros (TMSF) fornecidos a partir de determinados valores de faixas, minutos, segundos e quadros.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- Multimídia MCI_MAKE_TMSF macro do Windows
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770161"
---
# <a name="mci_make_tmsf-macro"></a>\_Macro Make \_ TMSF do MCI

O **MCI \_ Make \_ TMSF** macro cria um valor de tempo no formato de faixas/minutos/segundos/quadros (TMSF) fornecidos a partir de determinados valores de faixas, minutos, segundos e quadros.

## <a name="syntax"></a>Sintaxe


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*faixas* 
</dt> <dd>

Número de faixas.

</dd> <dt>

*alguns* 
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

## <a name="return-value"></a>Retornar valor

Retorna o tempo no formato TMSF empacotado.

## <a name="remarks"></a>Comentários

O tempo no formato TMSF é expresso como um valor **DWORD** com o byte menos significativo contendo faixas, o próximo byte menos significativo que contém minutos, o próximo byte menos significativo que contém segundos e o byte mais significativo contendo quadros.

A **macro \_ Make \_ TMSF do MCI** é definida da seguinte maneira:


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
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

 

 





