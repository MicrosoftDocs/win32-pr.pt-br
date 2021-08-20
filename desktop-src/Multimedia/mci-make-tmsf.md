---
title: Macro MCI_MAKE_TMSF (Mciapi. h)
description: O MCI \_ Make \_ TMSF macro cria um valor de tempo no formato de faixas/minutos/segundos/quadros (TMSF) fornecidos a partir de determinados valores de faixas, minutos, segundos e quadros.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- macro de MCI_MAKE_TMSF Windows multimídia
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
ms.openlocfilehash: ec038e0eb1e46c46162c9a2139f03881689db5fe1ee5993a8e135e5d92d67984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138399"
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

*controla* 
</dt> <dd>

Número de faixas.

</dd> <dt>

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

 

 





