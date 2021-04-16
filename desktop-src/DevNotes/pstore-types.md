---
description: Os tipos de dados para métodos de armazenamento protegidos.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Tipos de Pstore (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751550"
---
# <a name="pstore-types"></a>Tipos de Pstore

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Os tipos de dados para métodos de armazenamento protegidos.


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

**acesso ao PST \_**
</dt> <dd>

Define o modo de leitura ou gravação da regra de acesso.

</dd> <dt>

**\_ACCESSCLAUSETYPE PST**
</dt> <dd>

Define o tipo de cláusula da regra de acesso.

</dd> <dt>

**\_chave PST**
</dt> <dd>

Define a chave para o item armazenado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
