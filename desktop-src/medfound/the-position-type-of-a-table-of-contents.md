---
description: O tipo de posição de um índice
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: O tipo de posição de um índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f94f23e185b46f52123a80a0d27f7fefffcaff7e711a5e9718e07dab7da40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237890"
---
# <a name="the-position-type-of-a-table-of-contents"></a>O tipo de posição de um índice

Alguns métodos da interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) têm um parâmetro chamado *enumTocPosType* que tem um tipo de TIPO [**DE POS DE TOC \_ \_ de enum.**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type) Esse parâmetro especifica a posição em um arquivo de mídia em que um tabela de conteúdo é armazenada. A intenção era que o tabela de conteúdo pudesse ser armazenado no header do arquivo ou no corpo do arquivo como um objeto de nível superior. Essa funcionalidade ainda não foi implementada.

Atualmente, as tabelas de conteúdo só podem ser armazenadas como objetos de nível superior, portanto, você sempre deve definir o parâmetro *enumTocPosType* como **TOC \_ POS \_ TOPLEVELOBJECT.** Se você definir *enumTocPosType como* **TOC \_ POS \_ INHEADER,** o método retornará **E \_ NOTIMPL.**

Os métodos a seguir têm *um parâmetro enumTocPosType.*

-   [**GetTocCount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**GetTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**RemoveTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**RemoveTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de Programação do Analisador de Tabela de Conteúdo](toc-parser-programming-guide.md)
</dt> </dl>

 

 



