---
title: A função named_type_free_inst de dados
description: Os stubs chamam a função \_ \_ inst livre \_ de tipo nomeado para liberar memória associada ao tipo transmitido.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa55e896b89fccc513795a62634e805c2ad6e21b7bdecdd99a0b9cfe2d71cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016878"
---
# <a name="the-named_type_free_inst-function"></a>A função \_ \_ inst livre \_ de tipo nomeado

Os stubs chamam a **função \_ \_ \_ inst livre de tipo** nomeado para liberar memória associada ao tipo transmitido. A função é definida como:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

O parâmetro aponta para a instância do tipo transmitido. Esse objeto não deve ser liberado. Para uma discussão sobre quando chamar a função, consulte [O representar \_ como atributo](the-represent-as-attribute.md).

 

 




