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
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769279"
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

**PB**
</dt> <dd>

Um ponteiro para um **byte** que contém o blob, no formato [*PKCS \# 12*](../secgloss/p-gly.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**\_cadeia de \_ caracteres Unicode KEYSVC**](keysvc-unicode-string.md)
</dt> </dl>

 

 
