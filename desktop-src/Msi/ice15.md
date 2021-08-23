---
description: ICE15 valida que as referências de tipo de conteúdo e extensão nas tabelas MIME e Extensão são recíprocas. A tabela MIME deve referenciar um tipo de conteúdo a uma extensão que a tabela Extensão referencia de volta ao mesmo tipo de conteúdo.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e5e54dedd2663a9f849abee43e244c73d7aa5835426be05d4e0163f599ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529306"
---
# <a name="ice15"></a>ICE15

ICE15 valida que as referências de tipo de conteúdo e extensão nas tabelas [MIME](mime-table.md) e [Extensão](extension-table.md) são recíprocas. A tabela MIME deve referenciar um tipo de conteúdo a uma extensão que a tabela Extensão referencia de volta ao mesmo tipo de conteúdo.

Várias extensões podem referenciar o mesmo tipo MIME, desde que o tipo MIME referencia de volta a uma das extensões. Vários tipos MIME podem referenciar a mesma extensão, desde que a extensão seja referenciada de volta a um dos tipos MIME.

Observe que sempre que um MIME referencia uma extensão, essa extensão não pode ter a coluna MIME na tabela Extensão \_ definida como Null.

## <a name="result"></a>Resultado

ICE15 postará um erro se o tipo de conteúdo e as referências de extensão não são recíprocas.

## <a name="example"></a>Exemplo

ICE15 posta duas mensagens de erro para o exemplo mostrado:

-   O tipo de conteúdo test/x-chromes na tabela MIME faz referência à extensão tst, mas o tst de extensão na tabela Extensão faz referência a remos/x-remos. Isso não é recíproco.
-   O tipo de conteúdo faz referência ao flp de extensão, mas essa extensão tem uma entrada Null na coluna MIME da \_ tabela Extension.

[Tabela MIME](mime-table.md) (parcial)



| ContentType   | Extensão\_ |
|---------------|-------------|
| test/x-test   | Tst         |
| colchões/x-colchões | Flp         |



 

[Tabela de extensão](extension-table.md) (parcial)



| Extensão | Mime\_        |
|-----------|---------------|
| Tst       | colchões/x-colchões |
| Flp       | Nulo          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



