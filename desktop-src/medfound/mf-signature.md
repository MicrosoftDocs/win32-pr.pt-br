---
description: Contém uma assinatura de GRL (lista de revogação global).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Estrutura de MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171605"
---
# <a name="mf_signature-structure"></a>\_Estrutura de assinatura MF

Contém uma assinatura de GRL (lista de revogação global).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwSignVer**
</dt> <dd>

O número de versão da assinatura.

</dd> <dt>

**cbSign**
</dt> <dd>

O tamanho da assinatura em bytes.

</dd> <dt>

**rgSign**
</dt> <dd>

Uma matriz de bytes de tamanho **cbSign** que contém a assinatura. O tamanho real da matriz é maior do que o tamanho fornecido na declaração de estrutura.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é declarada em um cabeçalho do SDK. Para usar essa estrutura, adicione a declaração mostrada aqui ao seu código-fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Revogação de certificado OPM](opm-certificate-revocation.md)
</dt> <dt>

[Estruturas OPM](opm-structures.md)
</dt> </dl>

 

 




