---
title: Macro MCI_MSF_MINUTE (Mciapi. h)
description: A macro de minuto do MSF do MCI \_ \_ recupera o componente de minutos de um parâmetro que contém informações de minutos/segundos/quadros compactados (MSF).
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- macro de MCI_MSF_MINUTE Windows multimídia
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8423e63c7e155c072b496a9bf13c332619f96e8c6780cac6fae266f6a924c9f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039136"
---
# <a name="mci_msf_minute-macro"></a>Macro de minuto do \_ MSF MCI \_

A macro de **\_ \_ minuto do MSF do MCI** recupera o componente de minutos de um parâmetro que contém informações de minutos/segundos/quadros compactados (MSF).

## <a name="syntax"></a>Sintaxe


```C++
BYTE MCI_MSF_MINUTE(
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

Retorna o componente de minutos das informações de MSF especificadas.

## <a name="remarks"></a>Comentários

O tempo no formato MSF é expresso como um valor **DWORD** com o byte menos significativo contendo minutos, o próximo byte menos significativo que contém segundos e o próximo byte menos significativo que contém quadros. O byte mais significativo não é usado.

A macro de **\_ \_ minuto do MSF do MCI** é definida da seguinte maneira:


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
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

 

 





