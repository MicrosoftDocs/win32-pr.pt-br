---
title: Uniões encapsuladas
description: Uma união contida com seu discriminante em uma estrutura dentro é uma união encapsulada.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- tipos de dados MIDL, uniões encapsuladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc8f8f830d49430551af7d6450b0174742b9436afcdba764e9fa6494c957d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895356"
---
# <a name="encapsulated-unions"></a>Uniões encapsuladas

Uma união contida com seu discriminante em uma estrutura dentro é uma união encapsulada. A união encapsulada é indicada pela presença da palavra-chave [**switch.**](switch.md) Esse tipo de união é chamado porque o compilador MIDL encapsula automaticamente a união e seu discriminante em uma estrutura para transmissão durante uma chamada de procedimento remoto.

Se a marca de união estiver ausente (U1 TYPE no exemplo acima), o compilador gerará a estrutura com o campo de união \_ chamado *união \_ marcada*.

A forma de uniões deve ser a mesma entre plataformas para garantir a interconectividade.

Para ver uma descrição da forma de uma união encapsulada, consulte [**union**](union.md).

## <a name="examples"></a>Exemplos

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

Para obter informações relacionadas, consulte [MidL Base Types](midl-base-types.md), [**char**](char-idl.md), context handle , enum , first is **\[** [**\_**](context-handle.md), **\]** [](enum.md) **\[** [**\_**](first-is.md) **\]** **\[** [](handle.md) **\]** handle , **\[** [](ignore.md) **\]** ignore , [**int**](int.md), **\[** [**ignore**](ignore.md), **\]** last **\[** [**\_ is**](last-is.md) **\]** , length **\[** [**\_ is**](length-is.md) **\]** , max **\[** [**\_ is**](max-is.md) **\]** , **\[** [**ms \_ union**](ms-union-attrib.md) **\]** , [Nonencapsulated Unions](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , ref , **\[** [**size**](ref.md) **\]** **\[** [**\_ is**](size-is.md) **\]** , **\[** [**string**](string.md) **\]** , [**struct**](struct.md), [**switch**](switch.md) **\[** [**\_**](switch-is.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** [](union.md) **\[** [](unique.md) is , switch is , switch type , transmit as , union e unique **\]**

 

 




