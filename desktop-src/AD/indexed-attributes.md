---
title: Atributos indexados (AD DS)
description: Os atributos podem ser indexados. A indexação de um atributo pode melhorar o desempenho de consultas para esse atributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- AD de Atributos Indexados
- Atributos AD , indexados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd205fea66b198096a9a9427822eb4ba0ccb609fb3e6fef0854fa91848371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187580"
---
# <a name="indexed-attributes-ad-ds"></a>Atributos indexados (AD DS)

Os atributos podem ser indexados. A indexação de um atributo pode melhorar o desempenho de consultas para esse atributo.

Um atributo é indexado quando o [**atributo searchFlags**](/windows/desktop/ADSchema/a-searchflags) na definição de esquema do atributo tem o bit menos significativo definido como 1. Definir o bit menos significativo da definição de esquema de atributo **searchFlags** como 1 criará dinamicamente um índice. Definir o bit menos significativo da definição de esquema de atributo **searchFlags** como 0 fará com que o índice do atributo seja removido. O índice será criado automaticamente por um thread em segundo plano no controlador de domínio.

O ideal é que os atributos indexados sejam com valor único com valores altamente exclusivos distribuídos uniformemente no conjunto de instâncias. Quanto menos exclusivos os valores de um atributo são, menos efetivo será o índice.

Atributos com vários valores também podem ser indexados, mas o custo para criar o índice para um atributo com vários valores é maior em termos de armazenamento, atualização e tempo de pesquisa. O requisito de exclusividade para uma propriedade com vários valores é o mesmo que para uma propriedade de valor único– quanto mais exclusivos os valores são, mais eficaz é o índice.

Quanto mais atributos indexados uma classe tiver, mais tempo será necessário para criar novas instâncias da classe.

Os índices se aplicam a atributos, não a classes. Ou seja, quando um atributo é marcado como indexado, todas as instâncias do atributo são adicionadas ao índice, não apenas às instâncias que são membros de uma classe específica.

Para verificar se um servidor está usando um índice para processar uma consulta, de definido o seguinte valor do Registro em um controlador de domínio como 4. Em seguida, execute uma consulta nesse controlador de domínio e procure no log de eventos do diretório dados sobre os índices, se algum, usados para processar a consulta.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Para obter mais informações sobre outros bits na [**propriedade searchFlags,**](/windows/desktop/ADSchema/a-searchflags) consulte [Características de atributos](characteristics-of-attributes.md).

 

 