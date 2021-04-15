---
description: O \_ tipo de \_ Enumeração tipos de mensagem SMS descreve o tipo de conteúdo de uma mensagem de SMS (serviço de mensagens curtas).
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Enumeração de SMS_MESSAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761637"
---
# <a name="sms_message_types-enumeration"></a>Enumeração de tipos de \_ mensagem SMS \_

O tipo de enumeração **\_ \_ tipos de mensagem SMS** descreve o tipo de conteúdo de uma mensagem de SMS (serviço de mensagens curtas).

## <a name="syntax"></a>Syntax


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**\_mensagem de texto SMS \_**
</dt> <dd>

Uma mensagem de texto.

</dd> <dt>

<span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**\_mensagem de binário do SMS \_**
</dt> <dd>

Uma mensagem binária.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pelo comando [**de \_ \_ \_ envio de SMS do comando WPD**](wpd-command-sms-send-command.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




