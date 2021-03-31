---
title: Usando subclasses de tema
description: As classes de tema que representam controles como ComboBox, Edit, ExplorerBar, Rebar, Tab e Toolbar podem ser subclasses para fornecer variações de tema para esse controle específico.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635751"
---
# <a name="using-theme-subclasses"></a>Usando subclasses de tema

As classes de tema que representam controles como ComboBox, Edit, ExplorerBar, Rebar, Tab e Toolbar podem ser subclasses para fornecer variações de tema para esse controle específico. Por exemplo, a classe **Button** é uma subclasse como `Start::Button` para fornecer controle sobre o tema aplicado ao botão **Iniciar** .

> [!Note]  
> Tenha cuidado ao criar subclasses como as que são discutidas neste tópico. Como as subclasses podem ser alteradas ou não estar disponíveis nas versões subsequentes do Windows, você não é incentivado de usá-las.

 

## <a name="two-ways-to-use-a-theme-subclass"></a>Duas maneiras de usar uma subclasse de Theme

Um aplicativo pode usar um tema de subclasse de uma destas duas maneiras:

-   Ele pode usar a função [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) com uma cadeia de caracteres do formulário `subclass::class` no parâmetro *pszClassList* .
-   Ele pode chamar [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) com o nome da subclasse do tema no parâmetro *pszSubAppName* .

## <a name="using-theme-messages-that-set-visual-style"></a>Usando mensagens de tema que definem o estilo visual

Determinados controles, como Rebar e Toolbar, fornecem mensagens específicas que você pode enviar para instruir o controle a usar uma subclasse de tema. Para esses controles, forneça um ponteiro para um buffer que contém o nome da subclasse do tema no parâmetro *lParam* da mensagem. Use a mensagem de [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) genérica ou use uma variante específica como as mostradas na tabela a seguir.



| Control    | Mensagem                                             |
|------------|-----------------------------------------------------|
| Dica de ferramenta    | [**TTM \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   |
| Barra de ferramentas    | [**TB de \_ SETWINDOWTHEME**](tb-setwindowtheme.md)     |
| Rebar      | [**\_SETWINDOWTHEME RB**](rb-setwindowtheme.md)     |
| ComboBoxEx | [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md) |



 

A tabela a seguir lista algumas das subclasses que o Windows Vista define.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Classe</th>
<th>Subclasses</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ComboBox</td>
<td><ul>
<li>Endereço</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>Editar</td>
<td><ul>
<li>Endereço</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>InactiveSearchBoxEdit</li>
<li>InactiveSearchBoxEditComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
<li>MaxInactiveSearchBoxEdit</li>
<li>MaxInactiveSearchBoxEditComposited</li>
<li>MaxSearchBoxEdit</li>
<li>MaxSearchBoxEditComposited</li>
<li>SearchBoxEdit</li>
<li>SearchBoxEditComposited</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rebar</td>
<td><ul>
<li>BrowserTabBar</li>
<li>InactiveNavbar</li>
<li>InactiveNavbarComposited</li>
<li>MaxInactiveNavbar</li>
<li>MaxInactiveNavbarComposited</li>
<li>MaxNavbar</li>
<li>MaxNavbarComposited</li>
<li>Barra de navegação</li>
<li>NavbarComposited</li>
<li>NavbarNonTopmost</li>
</ul></td>
</tr>
<tr class="even">
<td>Tab</td>
<td><ul>
<li>BrowserTab</li>
</ul></td>
</tr>
<tr class="odd">
<td>Barra de ferramentas</td>
<td><ul>
<li>Go</li>
<li>GoComposited</li>
<li>InactiveGo</li>
<li>InactiveGoComposited</li>
<li>MaxGo</li>
<li>MaxGoComposited</li>
<li>MaxInactiveGo</li>
<li>MaxInactiveGoComposited</li>
<li>SearchButton</li>
<li>SearchButtonComposited</li>
<li>Viagem</li>
<li>TravelComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a>Subclasses do Internet Explorer

No Windows Vista, as subclasses de determinadas classes internas ao Windows Internet Explorer e ao Windows Explorer estão disponíveis, embora as próprias classes não sejam. A tabela a seguir lista as subclasses disponíveis.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AddressBand</td>
<td><ul>
<li>AB</li>
<li>ABGreen</li>
<li>ABGreenComposited</li>
<li>ABRed</li>
<li>ABRedComposited</li>
<li>ABYellow</li>
<li>ABYellowComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>Caixa de pesquisa</td>
<td><ul>
<li>InactiveSearchBox</li>
<li>InactiveSearchBoxComposited</li>
<li>MaxInactiveSearchBox</li>
<li>MaxInactiveSearchBoxComposited</li>
<li>MaxSearchBox</li>
<li>MaxSearchBoxComposited</li>
<li>SearchBoxComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

A tabela a seguir mostra as especificidades dessas classes.



| Control     | Parte         | Estados                                                 |
|-------------|--------------|--------------------------------------------------------|
| ADDRESSBAND | ABBACKGROUND | NORMAL (0x1), quente (0x2), DESABILITAdo (0x3), com foco (0x4) |
| SEARCHBOX   | SBBACKGROUND | NORMAL (0x1), quente (0x2), DESABILITAdo (0x3), com foco (0x4) |



 

 

 




