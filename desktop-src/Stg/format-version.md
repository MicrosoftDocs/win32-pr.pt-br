---
title: Versão de formato
description: O valor da versão de formato é um tipo de dados do WORD que é usado para indicar a versão de formato desse fluxo.
ms.assetid: 38362a45-4f49-4a85-aabe-452ff32c2812
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503019a3bfe3224e4137ac3bfd43fadbe1e15a3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499079"
---
# <a name="format-version"></a>Versão de formato

O valor da versão de formato é um tipo de dados do **Word** que é usado para indicar a versão de formato desse fluxo. Ele pode ser zero ou um. O indicador de versão de formato deve ser verificado durante a leitura do conjunto de propriedades. Se não for zero ou um, o fluxo foi gravado em uma especificação diferente e não poderá ser lido pelo código desenvolvido de acordo com essa especificação.

Os conjuntos de propriedades com formato versão 1 são equivalentes à versão 0, com as seguintes adições:

-   **Nomes de propriedade diferenciar maiúsculas e minúsculas**. Os nomes de propriedade são armazenados na propriedade de dicionário reservado, [ID de propriedade 0](/windows/desktop/Stg/reserved-property-identifiers). Nos conjuntos de propriedades da versão 1, esses nomes podem diferenciar maiúsculas de minúsculas. A diferenciação de maiúsculas e minúsculas é determinada pela propriedade de comportamento reservado, [ID de propriedade 0x80000003](/windows/desktop/Stg/reserved-property-identifiers).
-   **Nomes de propriedade longos**. Os conjuntos de propriedades da versão 1, diferentemente dos conjuntos de propriedades da versão 0, não são limitados no comprimento dos nomes de propriedade. Consulte a [ID de propriedade 0](/windows/desktop/Stg/reserved-property-identifiers) para obter mais informações sobre nomes de propriedade.
-   **Tipos de propriedade**. Os conjuntos de propriedades da versão 1 podem conter todos os tipos de propriedade que podem ser mantidos em um conjunto de propriedades da versão 0, além de alguns tipos adicionais. Consulte a estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) para obter mais informações sobre esses tipos.

 

 