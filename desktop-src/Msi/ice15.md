---
description: ICE15 valida que o tipo de conteúdo e as referências de extensão nas tabelas MIME e de extensão são recíprocas. A tabela MIME deve referenciar um tipo de conteúdo para uma extensão que a tabela de extensão faz referência ao mesmo tipo de conteúdo.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011299"
---
# <a name="ice15"></a>ICE15

ICE15 valida que o tipo de conteúdo e as referências de extensão nas tabelas [MIME](mime-table.md) e de [extensão](extension-table.md) são recíprocas. A tabela MIME deve referenciar um tipo de conteúdo para uma extensão que a tabela de extensão faz referência ao mesmo tipo de conteúdo.

Várias extensões podem referenciar o mesmo tipo MIME, desde que o tipo MIME faça referência a uma das extensões. Vários tipos MIME podem fazer referência à mesma extensão, desde que a extensão faça referência a um dos tipos MIME.

Observe que sempre que um MIME faz referência a uma extensão, essa extensão não pode ter a \_ coluna MIME na tabela de extensão definida como NULL.

## <a name="result"></a>Resultado

ICE15 posta um erro se o tipo de conteúdo e as referências de extensão não forem recíprocos.

## <a name="example"></a>Exemplo

O ICE15 posta duas mensagens de erro para o exemplo mostrado:

-   O tipo de conteúdo Test/x-flaps na tabela MIME faz referência à extensão TST, mas a extensão TST na tabela de extensão faz referência a flaps/x-flaps. Isso não é recíproco.
-   O tipo de conteúdo flaps/x-flaps faz referência à extensão FLP, mas essa extensão tem uma entrada nula na \_ coluna MIME da tabela de extensão.

[Tabela MIME](mime-table.md) (parcial)



| ContentType   | Extensão\_ |
|---------------|-------------|
| teste/x-teste   | TST         |
| flaps/x-flaps | FLP         |



 

[Tabela de extensão](extension-table.md) (parcial)



| Extensão | MIME\_        |
|-----------|---------------|
| TST       | flaps/x-flaps |
| FLP       | Nulo          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



