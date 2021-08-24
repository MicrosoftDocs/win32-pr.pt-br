---
description: O tipo de enumeração WPD \_ BITRATE TYPES descreve um tipo de compactação de \_ arquivos de áudio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: WPD_BITRATE_TYPES enumeração (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5b50b56222014119a50c9d4ecb0fd7eb96694b30f35fbcbb72dc6550fdf88606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704046"
---
# <a name="wpd_bitrate_types-enumeration"></a>Enumeração WPD \_ BITRATE \_ TYPES

O **tipo de enumeração WPD \_ BITRATE \_ TYPES** descreve o tipo de compactação de um arquivo de áudio.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**TIPO DE TAXA DE BITS WPD \_ \_ \_ NÃOUSADO**
</dt> <dd>

Esse valor não foi especificado.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**TIPO DE TAXA DE BITS WPD \_ \_ \_ DISCRETO**
</dt> <dd>

Compactação de taxa de bits constante.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**VARIÁVEL DE TIPO \_ DE TAXA \_ DE BITS WPD \_**
</dt> <dd>

Compactação de taxa de bits variável.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**TIPO DE TAXA DE BITS WPD \_ \_ \_ LIVRE**
</dt> <dd>

Taxa de bits de formato livre. Essa é uma taxa de bits constante que é menor que a taxa de bits máxima permitida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




