---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292854"
---
# <a name="elementhasnoname"></a>ElementHasNoName

## <a name="text"></a>Texto

O elemento não tem nome

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Um elemento não tem um nome. Por exemplo, o elemento não tem accName implementado e uma cadeia de caracteres vazia é retornada quando o método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) é usado para recuperar o nome de MSAA do elemento.

Esse problema causa problemas para as pessoas que dependem de um leitor de tela e teclado para navegação porque um elemento pode ser identificado incorretamente para o usuário.

## <a name="possible-causes"></a>Possíveis causas

-   O elemento ou seu pai não tem nome ou rótulo.
-   O elemento é atribuído a um [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) que sugere que o elemento tenha um nome.
-   O elemento que tem o foco não deve receber o foco. Por exemplo, um rótulo ou um controle desabilitado.
-   Um controle invisível recebeu o foco.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriedade Name](name-property.md)
</dt> </dl>

 

 




