---
description: Os tipos de dados para métodos Armazenamento protegidos.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Tipos PStore (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6def89ea4beb5d27a98cb8e6f44fc12271de7d1642b236f31f4979ed26b54a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538446"
---
# <a name="pstore-types"></a>Tipos PStore

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Os tipos de dados para métodos Armazenamento protegidos.


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

**PST \_ ACCESSMODE**
</dt> <dd>

Define o modo de leitura ou gravação da regra de acesso.

</dd> <dt>

**PST \_ ACCESSCLAUSETYPE**
</dt> <dd>

Define o tipo de cláusula da regra de acesso.

</dd> <dt>

**PST \_ KEY**
</dt> <dd>

Define a chave para o item armazenado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore.h</dt> </dl> |



 

 
