---
title: Expondo Owner-Drawn itens da caixa de listagem
description: Os desenvolvedores de aplicativos não precisam implementar o IAccessible para expor os itens em uma caixa de listagem desenhada pelo proprietário que tem o estilo LBS \_ HASSTRINGS porque a Microsoft acessibilidade ativa expõe os itens em caixas de listagem com esse estilo.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fed68477680376373da6c16f59b3fb556b6a435f15f04daae8f3f1262829dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115269"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Expondo Owner-Drawn itens da caixa de listagem

Os desenvolvedores de aplicativos não precisam implementar o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para expor os itens em uma caixa de listagem desenhada pelo proprietário que tem o estilo **lbs \_ HASSTRINGS** porque a Microsoft acessibilidade ativa expõe os itens em caixas de listagem com esse estilo. Os itens em uma caixa de listagem desenhada pelo proprietário com o estilo de **lbs \_ HASSTRINGS** são exibidos como texto. No entanto, esse estilo também é usado com caixas de listagem desenhadas pelo proprietário que não exibem texto para que os itens da caixa de listagem sejam expostos pelo Microsoft Acessibilidade Ativa.

Para permitir que o Microsoft Acessibilidade Ativa exponha os itens em uma caixa de listagem desenhada pelo proprietário que não exibe texto:

-   Use o estilo de **\_ HASSTRINGS lbs** ao criar a caixa de listagem.
-   Crie um equivalente textual que nomeia ou descreve cada item na caixa de listagem.
-   Ao adicionar itens à caixa de listagem desenhada pelo proprietário, use a mensagem do [lb \_ AddString](../controls/lb-addstring.md) para adicionar o texto que você deseja que o Microsoft acessibilidade ativa expor. Esse texto não é exibido, portanto, não faz parte dos dados desenhados pelo proprietário. Adicione os dados do item desenhado pelo proprietário usando a mensagem [ \_ SETITEMDATA de lb](../controls/lb-setitemdata.md) .

Ao usar o método acima, observe o seguinte:

-   Se você usar o estilo de **\_ classificação lbs** , a caixa de listagem será classificada usando as cadeias de caracteres fornecidas e não o procedimento de retorno de chamada do [WM \_ COMPAREITEM](../controls/wm-compareitem.md) .
-   Com as caixas de lista de variáveis desenhadas pelo proprietário criadas com o estilo **lbs \_ OwnerDrawVariable**, use uma variável global ou algum outro mecanismo para controlar quando o **membro de dados** de [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct) é válido. A variável global é necessária porque o sistema envia a mensagem do [WM \_ MEASUREITEM](../controls/wm-measureitem.md) assim que a cadeia de caracteres é adicionada, mas antes de os dados do item serem anexados e, nesse ponto, o membro de itens de **dados** não é válido.
-   Para alterar a cadeia de caracteres de um item em uma caixa de listagem com o estilo de **lbs \_ HASSTRINGS** , exclua o item com a mensagem de [ \_ exclusão de lb](../controls/lb-deletestring.md) e adicione a nova cadeia de caracteres com a mensagem do lb \_ AddString.

 

 