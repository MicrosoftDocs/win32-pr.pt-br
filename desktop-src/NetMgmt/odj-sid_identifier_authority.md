---
title: SID_IDENTIFIER_AUTHORITY
description: Definição de IDL de SID_IDENTIFIER_AUTHORITY
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104084986"
---
# <a name="sid_identifier_authority-structure"></a>Estrutura de SID_IDENTIFIER_AUTHORITY

Contém uma autoridade de identificador SID.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a>Membros

### <a name="value"></a>Valor

Deve ser definido como os seis bytes da autoridade do identificador SID.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)