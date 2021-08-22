---
description: Identifica o conjunto de regras de acesso para os dados de armazenamento protegido.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: Estrutura de PST_ACCESSRULESET (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 9695af01c6f0ffb33fe20a112659444011ad9c18812b8d2fd885641635c6b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666972"
---
# <a name="pst_accessruleset-structure"></a>Estrutura de ACCESSRULESET de PST \_

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Identifica o conjunto de regras de acesso para os dados de armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho desta estrutura.

</dd> <dt>

**cRules**
</dt> <dd>

O número de regras na matriz **rgRules** .

</dd> <dt>

**rgRules**
</dt> <dd>

Um ponteiro para uma matriz de [**estruturas \_ ACCESSRULE de PST**](pst-accessrule.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ACCESSRULE PST**](pst-accessrule.md)
</dt> <dt>

[**CreateSubtype**](ipstore-createsubtype.md)
</dt> </dl>

 

 
