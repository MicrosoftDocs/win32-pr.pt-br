---
title: ODJ_SID
description: Definição de IDL de ODJ_SID
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104008555"
---
# <a name="odj_sid-structure"></a>Estrutura de ODJ_SID

Contém um SID (identificador de segurança).

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a>Membros

### <a name="revision"></a>Revisão

Deve ser definido como a revisão de SID.

### <a name="subauthoritycount"></a>SubAuthorityCount

Deve ser definido como o número de elementos na subautoridade.

### <a name="identifierauthority"></a>IdentifierAuthority

Deve ser definido como o identificador de autoridade SID.

### <a name="subauthority"></a>Subautoridade

Deve conter uma matriz de subautoridades SID.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**\_autoridade de \_ identificador \_ Sid ODJ**](odj-sid_identifier_authority.md)
