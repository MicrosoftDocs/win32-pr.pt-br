---
title: Macro MCI_MAKE_MSF (Mciapi. h)
description: O MCI \_ criar \_ macro do MSF cria um valor de tempo no formato de minutos/segundos/quadros empacotado a partir dos minutos, segundos e valores de quadro determinados.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- Multimídia MCI_MAKE_MSF macro do Windows
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
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919142"
---
# <a name="mci_make_msf-macro"></a>\_Macro do \_ MSF Make MCI

O **MCI \_ criar \_** macro do MSF cria um valor de tempo no formato de minutos/segundos/quadros empacotado a partir dos minutos, segundos e valores de quadro determinados.

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

Retorna o tempo no formato empacotado do MSF.

## <a name="remarks"></a>Comentários

O tempo no formato MSF é expresso como um valor **DWORD** com o byte menos significativo contendo minutos, o próximo byte menos significativo que contém segundos e o próximo byte menos significativo que contém quadros. O byte mais significativo não é usado.

O **MCI \_ criar \_** macro do MSF é definido da seguinte maneira:


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
| Cabeçalho<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Macros MCI](mci-macros.md)
</dt> </dl>

 

 





