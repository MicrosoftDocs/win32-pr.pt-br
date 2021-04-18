---
title: Expondo Owner-Drawn itens da caixa de combinação
description: Os desenvolvedores de aplicativos não precisam implementar o IAccessible para expor os itens em uma caixa de combinação desenhada pelo proprietário que tem o estilo CBS \_ HASSTRINGS porque o Microsoft acessibilidade ativa expõe os itens em caixas de combinação com esse estilo.
ms.assetid: 9ff14b2f-ae09-4839-b281-fba46addaf5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364dccaf21927e2d0092fc744d501f47830c6eeb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105757347"
---
# <a name="exposing-owner-drawn-combo-box-items"></a>Expondo Owner-Drawn itens da caixa de combinação

Os desenvolvedores de aplicativos não precisam implementar o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para expor os itens em uma caixa de combinação desenhada pelo proprietário que tem o estilo **CBS \_ HASSTRINGS** porque o Microsoft acessibilidade ativa expõe os itens em caixas de combinação com esse estilo. Os itens em uma caixa de combinação desenhada pelo proprietário com o estilo **CBS \_ HASSTRINGS** são exibidos como texto. No entanto, esse estilo também é usado com caixas de combinação desenhadas pelo proprietário que não exibem texto para que os itens da caixa de combinação sejam expostos pelo Microsoft Acessibilidade Ativa.

Para permitir que o Microsoft Acessibilidade Ativa exponha os itens em uma caixa de combinação desenhada pelo proprietário que não exibe texto:

-   Use o estilo **CBS \_ HASSTRINGS** ao criar a caixa de combinação.
-   Crie um equivalente textual que nomeia ou descreve cada item na caixa de combinação.
-   Ao adicionar itens à caixa de combinação desenhada pelo proprietário, use a \_ mensagem CREATESTRING CB para adicionar o texto que você deseja que o Microsoft acessibilidade ativa expor. Esse texto não é exibido, portanto, não deve fazer parte dos dados desenhados pelo proprietário. Adicione os dados do item desenhado pelo proprietário usando a \_ mensagem CB SETITEMDATA.

Ao usar o método acima, observe o seguinte:

-   Se você usar o estilo de **\_ classificação CBS** , a caixa de combinação será classificada usando as cadeias de caracteres fornecidas e não o procedimento de retorno de chamada do [WM \_ COMPAREITEM](../controls/wm-compareitem.md) .
-   Com as caixas de combinação da variável desenhada pelo proprietário criadas com o estilo **CBS \_ OwnerDrawVariable**, use uma variável global ou algum outro mecanismo para controlar quando o membro de **dados** de [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct) é válido. A variável global é necessária porque o sistema envia a mensagem do [WM \_ MEASUREITEM](../controls/wm-measureitem.md) assim que a cadeia de caracteres é adicionada, mas antes de os dados do item serem anexados e, nesse ponto, o membro de itens de **dados** não é válido.
-   Para alterar a cadeia de caracteres de um item em uma caixa de combinação com o estilo **\_ HASSTRINGS do CBS** , exclua o item com a mensagem [CB \_ excluirstring](../controls/cb-deletestring.md) e adicione a nova cadeia de caracteres à mensagem [CB \_ AddString](../controls/cb-addstring.md) .

 

 