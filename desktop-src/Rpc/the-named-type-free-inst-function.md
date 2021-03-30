---
title: A função named_type_free_inst
description: Os stubs chamam a \_ função de tipo nomeado \_ Free \_ Inst para liberar memória associada ao tipo transmitido.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635432"
---
# <a name="the-named_type_free_inst-function"></a>A \_ \_ \_ função instra gratuita de tipo nomeado

Os stubs chamam a função de **\_ tipo nomeado \_ Free \_ Inst** para liberar memória associada ao tipo transmitido. A função é definida como:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

O parâmetro aponta para a instância do tipo transmitido. Este objeto não deve ser liberado. Para obter uma discussão sobre quando chamar a função, consulte [o \_ atributo representar como](the-represent-as-attribute.md).

 

 




