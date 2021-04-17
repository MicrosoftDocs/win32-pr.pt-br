---
description: O tipo de posição de um sumário
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: O tipo de posição de um sumário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813348"
---
# <a name="the-position-type-of-a-table-of-contents"></a>O tipo de posição de um sumário

Alguns métodos da interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) têm um parâmetro chamado *enumTocPosType* que tem um tipo de [**tipo de PDV de Sumário de enumeração \_ \_**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type). Esse parâmetro especifica a posição em um arquivo de mídia em que um sumário é armazenado. A intenção era que o Sumário pudesse ser armazenado no cabeçalho do arquivo ou no corpo do arquivo como um objeto de nível superior. Essa funcionalidade ainda não foi implementada.

Atualmente, as tabelas de conteúdo só podem ser armazenadas como objetos de nível superior, portanto, você deve sempre definir o parâmetro *enumTocPosType* como **TOC \_ \_ TOPLEVELOBJECT do PDV**. Se você definir *enumTocPosType* como **índice \_ de \_ PDV de Sumário**, o método retornará **E \_ NOTIMPL**.

Os métodos a seguir têm um parâmetro *enumTocPosType* .

-   [**GetTocCount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**GetTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**RemoveTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**RemoveTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do analisador de Sumário](toc-parser-programming-guide.md)
</dt> </dl>

 

 



