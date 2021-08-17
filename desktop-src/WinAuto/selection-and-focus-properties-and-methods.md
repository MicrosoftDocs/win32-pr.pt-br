---
title: Propriedades e métodos de seleção e foco
description: Como muitos elementos em aplicativos em execução no Microsoft Windows sistemas operacionais, os objetos acessíveis selecionam e recebem o foco do teclado. Esses atributos permitem que os usuários interajam com elementos do aplicativo, alterem valores e os manipulem de outra forma.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf5c5bc4a60e664c124e7181f998d9e0a7af6ab82ef9b2d4f030f7541d530ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745225"
---
# <a name="selection-and-focus-properties-and-methods"></a>Propriedades e métodos de seleção e foco

Como muitos elementos em aplicativos em execução em sistemas operacionais microsoft Windows, os objetos acessíveis *selecionam* e recebem o foco do *teclado*. Esses atributos permitem que os usuários interajam com elementos do aplicativo, alterem valores e os manipulem de outra forma.

Há algumas diferenças importantes entre a seleção de objeto e o foco do objeto:

-   Um objeto focalizado é o objeto em todo o sistema operacional que recebe a entrada do teclado. O objeto com o foco do teclado é a janela ativa ou um objeto filho da janela ativa.
-   Um objeto selecionado é marcado para participar de algum tipo de operação de grupo.

Por exemplo, um usuário pode selecionar vários itens em um controle de exibição de lista, mas o foco é dado apenas a um objeto no sistema por vez. Observe que os itens focalizados são de uma seleção de itens.

Os clientes determinam se um determinado objeto acessível ou elemento filho tem o foco chamando [**IAccessible::get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus). Os clientes determinam se um objeto está selecionado ou quais filhos dentro de um objeto acessível são selecionados chamando [**IAccessible::get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection). Para objetos como controles de exibição de lista em que mais de um filho está selecionado, o objeto pai deve dar suporte à interface [IEnumVARIANT,](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) que permite que os clientes enumerem os filhos selecionados.

## <a name="events-triggered-in-menus"></a>Eventos disparados em menus

Microsoft Active Accessibility expõe menus padrão criados com as APIs de menu e os arquivos de recurso do Microsoft Win32. Para ser consistente com menus padrão, os servidores com menus personalizados disparam [**EVENT \_ OBJECT \_ FOCUS**](event-constants.md), não [**EVENT OBJECT \_ \_ SELECTION**](event-constants.md), quando um usuário realça um item de menu.

> [!Note]  
> Microsoft Active Accessibility dá suporte à seleção do texto contido em controles de edição e edição rich porque o texto é exposto como uma única cadeia de caracteres na propriedade [**Value**](value-property.md) para esses controles.

 

## <a name="in-this-section"></a>Nesta seção

-   [Selecionando objetos filho](selecting-child-objects.md)

 

 