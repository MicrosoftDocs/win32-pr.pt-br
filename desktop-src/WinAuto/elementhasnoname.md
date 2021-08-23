---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cde3597a0922159eb035e94e08691cf9d36a07f8a1c23ec0cb25280ab961faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829525"
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

 

 




