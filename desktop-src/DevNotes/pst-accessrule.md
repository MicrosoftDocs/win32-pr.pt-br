---
description: Descreve uma regra para o acesso a itens armazenados no armazenamento protegido.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: Estrutura de PST_ACCESSRULE (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749927"
---
# <a name="pst_accessrule-structure"></a>Estrutura de ACCESSRULE de PST \_

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Descreve uma regra para o acesso a itens armazenados no armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho desta estrutura.

</dd> <dt>

**AccessModeFlags**
</dt> <dd>

Os modos de acesso aos quais o conjunto especificado de cláusulas de acesso pertence.



| Valor                                                                                                                                                                                                         | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_ LER**</dt> <dt>0x0001</dt> </dl>    | Modo de acesso de leitura.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_**</dt> <dt>0X0002</dt> de gravação </dl> | Modo de acesso de gravação.<br/> |



 

</dd> <dt>

**cClauses**
</dt> <dd>

O número de estruturas na matriz **rgClauses** .

</dd> <dt>

**rgClauses**
</dt> <dd>

Um ponteiro para uma matriz de [**estruturas \_ ACCESSCLAUSE de PST**](pst-accessclause.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ACCESSCLAUSE PST**](pst-accessclause.md)
</dt> <dt>

[**\_ACCESSRULESET PST**](pst-accessruleset.md)
</dt> </dl>

 

 
