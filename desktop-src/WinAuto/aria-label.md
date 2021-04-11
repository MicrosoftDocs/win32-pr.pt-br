---
title: Erro de rótulo do ARIA
description: Erro de rótulo do ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1091c46dbb660c4c3568d24bfca34d94ef869f1e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104008534"
---
# <a name="aria-label-error"></a>Erro de rótulo do ARIA

## <a name="text"></a>Texto

O elemento é do tipo **entrada**, **botão**, **imagem-botão** ou **ponto de referência** , mas não tem um nome acessível.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Este erro se aplica a:

-   Campos de entrada de formulário:
    -   Marcas HTML —**tipo de entrada \[ = " \| caixa de seleção de senha de texto arquivo de \| \| rádio \| \| \| telefone \| de cor do Tel \| Data \| DateTime \| DateTime-local \| \| semana hora \| mês \| número intervalo de \| \| pesquisa \| URL \] "**, **Select**, **DataList** e **TextArea**.
    -   WAI-funções do ARIA —**CheckBox**, **ComboBox**, ListBox **, Radiogroup,**  **Radio**, **TextBox**, **Tree**, **Slider** e **SpinButton**.
-   Imagens/botões/botões de imagem
    -   Marcas HTML —**img**, **Input \[ Type = "Image \| Button" \]** e **Button**.
    -   WAI-funções do ARIA —**img** e **Button**.
-   Pontos de referência
    -   WAI-funções do ARIA —**região**, **faixa**, **complementar**, **ContentInfo**, **formulário**, **principal**, **navegação** e **pesquisa**.

> [!Note]  
> AccChecker mostra esse erro até mesmo para elementos para os quais o nome acessível é definido por padrão com base no conteúdo HTML interno (consulte o elemento **banner** no exemplo acima). Nesses casos, você pode suprimir esses erros.

 

Todos os elementos de interface do usuário semanticamente importantes, como campos de formulário (por exemplo, **entrada**, **seleção**, **TextArea**), imagens, botões e pontos de referência (marcas que representam regiões lógicas) devem ter o nome acessível para permitir que os leitores de tela os anunciem corretamente.

Para corrigir esse erro, defina o nome acessível de uma das seguintes maneiras (listadas na ordem de preferência).

-   Campos de formulário: Use a marca de **rótulo** e defina o atributo **para** como o valor de **ID** do campo de destino.
-   Botão de imagem/imagem: defina o atributo **ALT** .
-   Botões: defina o texto da legenda do botão.
-   Para qualquer elemento:
    -   atributo [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : Defina como o valor de **ID** do elemento que contém a cadeia de caracteres de nome acessível.
    -   atributo [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : definido como a cadeia de caracteres de nome acessível.
    -   atributo de [**título**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : Defina como a cadeia de caracteres de nome acessível (também crie uma **dica de ferramenta**).

## <a name="example"></a>Exemplo


```HTML
<!-- For landmark tags, set the accessible name by using the aria-labelledby 
attribute to reference the visible headers. -->
<h1 id="formHeader">Application Form</h1>
<form aria-labelledby="formHeader">

  <!-- For input fields, use the LABEL tag with the for attribute. -->
  <label for="fullName">Full Name</label>
  <input id="fullName" type="text" />

  <!-- If there is no visible text that can be referenced, set the accessible 
  name by using aria-label or title attributes. -->
  <input type="file" aria-label="Your photo"/>

  <!-- For images, use the alt attribute. -->
  <img src="…" alt="Uploaded photo" />

  <!-- For buttons, caption text is also used as the accessible name. -->
  <button onclick="processForm()">Send</button>

  <!-- For image buttons, use the alt attribute to define the accessible name. -->
  <input type="image" src="images/moreinfo.png" alt="Show more info"/>

  <!-- For elements with inner text this error can be suppressed because the 
  accessible name is set by default. -->
  <div role="banner">Accessible name set by default</div>
</form >
```



 

 




