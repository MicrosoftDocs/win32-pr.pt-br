---
description: Contém informações sobre a cláusula de acesso para o armazenamento protegido.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: Estrutura de PST_ACCESSCLAUSE (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: e5933b762ac19ac188e2d7253e86482caae968abd58ecb02087c32657d250216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386176"
---
# <a name="pst_accessclause-structure"></a>Estrutura de ACCESSCLAUSE de PST \_

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Contém informações sobre a cláusula de acesso para o armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho desta estrutura.

</dd> <dt>

**Cláusulatype**
</dt> <dd>

O tipo de dados apontado pelo membro **pbClauseData** . Para obter mais informações, consulte [**Pstore Types**](pstore-types.md).

</dd> <dt>

**cbClauseData**
</dt> <dd>

O tamanho dos dados apontados pelo membro **pbClauseData** .

</dd> <dt>

**pbClauseData**
</dt> <dd>

Um ponteiro para os dados da cláusula de acesso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ACCESSRULE PST**](pst-accessrule.md)
</dt> </dl>

 

 
