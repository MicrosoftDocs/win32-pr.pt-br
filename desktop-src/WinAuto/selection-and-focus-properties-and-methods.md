---
title: Propriedades e métodos de seleção e foco
description: Como muitos elementos em aplicativos executados em sistemas operacionais Microsoft Windows, os objetos acessíveis selecionam e recebem o foco do teclado. Esses atributos permitem que os usuários interajam com os elementos do aplicativo, alteram valores e os manipulam de outra forma.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641382"
---
# <a name="selection-and-focus-properties-and-methods"></a>Propriedades e métodos de seleção e foco

Como muitos elementos em aplicativos executados em sistemas operacionais Microsoft Windows, os objetos acessíveis *selecionam* e recebem o *foco* do teclado. Esses atributos permitem que os usuários interajam com os elementos do aplicativo, alteram valores e os manipulam de outra forma.

Há algumas diferenças importantes entre a seleção de objetos e o foco do objeto:

-   Um objeto focalizado é um objeto em todo o sistema operacional que recebe entrada de teclado. O objeto com o foco do teclado é a janela ativa ou um objeto filho da janela ativa.
-   Um objeto selecionado está marcado para participar de algum tipo de operação de grupo.

Por exemplo, um usuário pode selecionar vários itens em um controle de exibição de lista, mas o foco é fornecido somente a um objeto no sistema de cada vez. Observe que os itens focados são de uma seleção de itens.

Os clientes determinam se um determinado objeto acessível ou elemento filho tem o foco chamando [**IAccessible:: get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus). Os clientes determinam se um objeto está selecionado ou quais filhos dentro de um objeto acessível são selecionados, chamando [**IAccessible:: get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection). Para objetos como controles de exibição de lista em que mais de um filho é selecionado, o objeto pai deve dar suporte à interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , que permite aos clientes enumerar os filhos selecionados.

## <a name="events-triggered-in-menus"></a>Eventos disparados em menus

O Microsoft Acessibilidade Ativa expõe os menus padrão criados com as APIs de menu e os arquivos de recursos do Microsoft Win32. Para ser consistente com menus padrão, os servidores com menus personalizados disparam o [**\_ \_ foco do objeto de evento**](event-constants.md), não a [**\_ \_ seleção de objeto de evento**](event-constants.md), quando um usuário realça um item de menu.

> [!Note]  
> O Microsoft Acessibilidade Ativa não oferece suporte à seleção do texto contido em controles editar e Rich Edit porque o texto é exposto como uma única cadeia de caracteres na propriedade [**Value**](value-property.md) para esses controles.

 

## <a name="in-this-section"></a>Nesta seção

-   [Selecionando objetos filho](selecting-child-objects.md)

 

 