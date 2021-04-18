---
description: O \_ tipo de enumeração de tipos de taxa de bits WPD \_ descreve um tipo de compactação arquivos de áudio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Enumeração de WPD_BITRATE_TYPES (PortableDevice. h)
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
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791599"
---
# <a name="wpd_bitrate_types-enumeration"></a>\_Enumeração de tipos de taxa de bits WPD \_

O tipo de enumeração de **\_ \_ tipos de taxa de bits WPD** descreve o tipo de compactação de um arquivo de áudio.

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

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_tipo de taxa de bits WPD \_ \_ não utilizado**
</dt> <dd>

Este valor não foi especificado.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_tipo de taxa de bits WPD \_ \_ discreto**
</dt> <dd>

Compactação de taxa de bits constante.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**variável de tipo de taxa de \_ bits WPD \_ \_**
</dt> <dd>

Compactação de taxa de bits variável.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**\_tipo de taxa de bits WPD \_ \_ gratuito**
</dt> <dd>

Taxa de bits de formato livre. Essa é uma taxa de bits constante inferior à taxa máxima de bits permitida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




