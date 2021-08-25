---
description: A \_ estrutura de blob KEYSVC define um blob de serviço de chave. Essa estrutura é usada pela função RKeyPFXInstall.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: Estrutura de KEYSVC_BLOB (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 7e71a090558b31444c550146a2cb99f062080db9b80e7d69561ff891b93262b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992966"
---
# <a name="keysvc_blob-structure"></a>\_Estrutura de blob KEYSVC

A estrutura de **\_ blob KEYSVC** define um blob de serviço de chave. Essa estrutura é usada pela função [**RKeyPFXInstall**](rkeypfxinstall.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Membros

<dl> <dt>

**CB**
</dt> <dd>

Um valor **ULONG** que especifica o tamanho, em bytes, de **PB**.

</dd> <dt>

**pb**
</dt> <dd>

Um ponteiro para um **byte** que contém o blob, no formato [*PKCS \# 12*](../secgloss/p-gly.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**\_cadeia de \_ caracteres Unicode KEYSVC**](keysvc-unicode-string.md)
</dt> </dl>

 

 
