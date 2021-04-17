---
description: O \_ tipo de enumeração de tipos de codificação do SMS WPD \_ \_ descreve o tipo de codificação de uma mensagem de SMS (serviço de mensagens curtas).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Enumeração de WPD_SMS_ENCODING_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748677"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>\_Enumeração de \_ tipos de codificação de SMS WPD \_

O tipo de enumeração de **\_ tipos de \_ codificação \_ do SMS WPD** descreve o tipo de codificação de uma mensagem de SMS (serviço de mensagens curtas).

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**Codificação de SMS \_ \_ 7 \_ bits**
</dt> <dd>

Codificação de sete bits.

</dd> <dt>

<span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**Codificação de SMS \_ \_ 8 \_ bits**
</dt> <dd>

Codificação de oito bits.

</dd> <dt>

<span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**Codificação de SMS de \_ \_ UTF \_ 16**
</dt> <dd>

Codificação de 16 bits (UTF).

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [de \_ \_ codificação de SMS WPD](sms-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




