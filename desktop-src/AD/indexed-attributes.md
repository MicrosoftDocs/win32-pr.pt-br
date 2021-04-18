---
title: Atributos indexados (AD DS)
description: Os atributos podem ser indexados. A indexação de um atributo pode melhorar o desempenho de consultas para esse atributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- AD de atributos indexados
- Atributos AD, indexado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105751016"
---
# <a name="indexed-attributes-ad-ds"></a>Atributos indexados (AD DS)

Os atributos podem ser indexados. A indexação de um atributo pode melhorar o desempenho de consultas para esse atributo.

Os atributos são indexados quando o atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) na definição de esquema do atributo tem o bit menos significativo definido como 1. Definir o bit menos significativo da definição de esquema de atributo **searchFlags** como 1 criará um índice dinamicamente. Definir o bit menos significativo da definição de esquema de atributo **searchFlags** como 0 fará com que o índice do atributo seja removido. O índice será criado automaticamente por um thread em segundo plano no controlador de domínio.

O ideal é que os atributos indexados tenham um valor único com valores altamente exclusivos distribuídos uniformemente no conjunto de instâncias. Quanto menos únicos forem os valores de um atributo, menos efetivo será o índice.

Os atributos com valores múltiplos também podem ser indexados, mas o custo para criar o índice para um atributo com vários valores é maior em termos de armazenamento, atualização e tempo de pesquisa. O requisito de exclusividade para uma propriedade de valores múltiplos é o mesmo que para uma propriedade de valor único; quanto mais exclusivo, os valores são mais eficazes para o índice.

Quanto mais atributos indexados uma classe tiver, mais tempo será necessário para criar novas instâncias da classe.

Os índices se aplicam a atributos, e não a classes. Ou seja, quando um atributo é marcado como indexado, todas as instâncias do atributo são adicionadas ao índice, não apenas às instâncias que são membros de uma classe específica.

Para verificar se um servidor está usando um índice para processar uma consulta, defina o valor do registro a seguir em um controlador de domínio como 4. Em seguida, execute uma consulta nesse controlador de domínio e procure no log de eventos do diretório dados sobre os índices, se houver, usados para processar a consulta.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Para obter mais informações sobre outros bits na propriedade [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) , consulte [características de atributos](characteristics-of-attributes.md).

 

 