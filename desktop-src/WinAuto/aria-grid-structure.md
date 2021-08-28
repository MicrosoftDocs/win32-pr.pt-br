---
title: Erro de estrutura de grade do ARIA
description: Erro de estrutura de grade do ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b91010417ed01f211859839ceab124b299b10679b3d460f860c03e5b2473f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122376"
---
# <a name="aria-grid-structure-error"></a>Erro de estrutura de grade do ARIA

## <a name="text"></a>Texto

O elemento com a função **Grid** não tem uma estrutura de grade ou marcação acessível correspondente.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a elementos personalizados que têm o atributo **role** definido como "Grid". Ele não se aplica a marcas de tabela HTML que têm uma **função** implícita de "Grid".

Um elemento que tem seu atributo de **função** definido como "grade" deve ter a estrutura definida pela função de grade WAI-ARIA (aplicativos de Internet avançados) acessíveis, incluindo o nome acessível para a grade e seus subelementos de cabeçalho.

Para corrigir esse erro, examine sua implementação para garantir que ela esteja em conformidade com a especificação WAI-ARIA. Especificamente, verifique se a estrutura atende às regras a seguir.

-   a **grade** contém elementos **Row** ou **rowgroup** .
-   **rowgroup** contém elementos de **linha** .
-   os **elementos de** **linha** contêm elementos **ColumnHeader** ou **gridcell** ou rowgroup.

Um nome acessível deve ser definido para os elementos **Grid**, **ColumnHeader**, **gridcell** e **multiheader** usando um dos atributos a seguir.

-   atributo [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para referenciar o elemento que contém o texto.
-   atributo [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para definir o nome acessível diretamente.
-   [**título**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) para criar uma dica de ferramenta que é ao mesmo tempo usada como um nome.

 

 




