---
title: Erro de rótulo ARIA
description: Erro de rótulo ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42abee9028db8c3a4070d9b60d0650187339fc4c9ec34d0b70f720c27e973897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122316"
---
# <a name="aria-label-error"></a>Erro de rótulo ARIA

## <a name="text"></a>Texto

O elemento é do tipo **entrada**, **botão**, **botão de** imagem ou ponto de **referência,** mas não tem um nome acessível.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a:

-   Campos de entrada do formulário:
    -   Marcas HTML— input type= **"text password checkbox** radio file email tel color date **\[ \| \| \| \| \| \| \| \| \| datetime \| datetime-local time \| week month number range search \| \| \| \| \| \| url" \]**, **select**, datalist e **textarea**.
    -   Funções DE SINAL-ARIA **—** caixa de seleção , **caixa** de combinação , **caixa** de listagem , **radiogroup**, **rádio** **,** caixa de texto , **árvore,** **controle deslizante** e **botão de rotação**.
-   Botões/imagens/imagens
    -   Marcas HTML—**img**, **tipo de \[ entrada="botão \| de imagem" \]** e **botão**.
    -   Funções DE ARIA DEMOS –**img** e **botão**.
-   Pontos de referência
    -   Funções DE ARIA-MAPS —**região**, **faixa**, **complementar,** **contentinfo**, **formulário**, **principal,** **navegação** e **pesquisa**.

> [!Note]  
> O AccChecker mostra esse erro até mesmo para elementos para os quais o nome acessível é definido por padrão com base no conteúdo HTML interno (consulte o elemento **banner** no exemplo acima). Nesses casos, você pode suprimir esses erros.

 

Todos os elementos de interface do usuário semanticamente importantes, como campos de formulário (por **exemplo,** entrada **,** selecione , **área** de texto ), imagens, botões e pontos de referência (marcas que representam regiões lógicas) devem ter o nome acessível para permitir que os leitores de tela os anunam corretamente.

Para corrigir esse erro, de definir o nome acessível de uma das seguintes maneiras (listadas na ordem de preferência).

-   Campos de formulário: use **a marca de** rótulo e de definir o atributo **for** como o valor **da ID** do campo de destino.
-   Botão imagem/imagem: de definir o **atributo alt.**
-   Botões: de definir o texto da legenda do botão.
-   Para qualquer elemento:
    -   [**atributo aria-labelledby:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) definido como o **valor da ID** do elemento que contém a cadeia de caracteres de nome acessível.
    -   [**atributo aria-label:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) definido como a cadeia de caracteres de nome acessível.
    -   [**atributo title:**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) definido como a cadeia de caracteres de nome acessível (também crie uma **dica de ferramenta**).

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



 

 




