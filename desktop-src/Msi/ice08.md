---
description: ICE08 valida que a tabela de componentes não contém GUIDs duplicados. Cada componente deve ter um GUID exclusivo. Nenhuma validação será feita se a tabela de componentes não existir.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6075b7c895242fe5cfa7608a414643a9e3491787fc59037f8761fa66b18354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745316"
---
# <a name="ice08"></a>ICE08

ICE08 valida que a [tabela de componentes](component-table.md) não contém [GUIDs](guid.md)duplicados. Cada componente deve ter um GUID exclusivo. Nenhuma validação será feita se a tabela de componentes não existir.

## <a name="result"></a>Resultado

ICE08 posta uma mensagem de erro se duas ou mais entradas na coluna ComponentID da tabela de componentes contiverem o mesmo GUID.

## <a name="example"></a>Exemplo

No exemplo a seguir, ICE08 postaria uma mensagem informando que os componentes vermelho e verde têm GUIDs duplicados.

[Tabela de componentes](component-table.md) (parcial)



| Componente | ComponentId                            |
|-----------|----------------------------------------|
| Vermelho       | {0000000A-0003-0000-0000-624474736554} |
| Azul      | {0000000A-0003-0000-0000-624474736354} |
| Verde     | {0000000A-0003-0000-0000-624474736554} |



 

Para corrigir esse erro, altere qualquer um dos GUIDs duplicados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



