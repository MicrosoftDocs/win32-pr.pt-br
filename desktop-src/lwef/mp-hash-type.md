---
title: Enumeração de MP_HASH_TYPE (MpClient. h)
description: Tipos de hash possíveis.
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- recursos do ambiente de Windows herdado de enumeração de MP_HASH_TYPE
- Windows recursos de ambiente herdados do ponteiro de enumeração PMP_HASH_TYPE
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98e048b77953a90051de947b2b500c4ab1c07f29138418418edfdce5f5ebad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961226"
---
# <a name="mp_hash_type-enumeration"></a>Enumeração de tipo de \_ hash MP \_

Tipos de hash possíveis.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**\_tipo de hash MP \_ \_ None**
</dt> <dd>

Sem hash.

</dd> <dt>

<span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**\_Tipo de hash MP \_ \_ CRC32**
</dt> <dd>

CRC32

</dd> <dt>

<span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**\_Tipo de hash MP \_ \_ MD5**
</dt> <dd>

MD5

</dd> <dt>

<span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**\_Tipo de hash MP \_ \_ SHA1**
</dt> <dd>

SHA1

</dd> <dt>

<span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**\_Tipo de hash MP \_ \_ SHA256**
</dt> <dd>

SHA 256

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





