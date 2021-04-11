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
# <a name="aria-label-error"></a><span data-ttu-id="6cf51-104">Erro de rótulo do ARIA</span><span class="sxs-lookup"><span data-stu-id="6cf51-104">ARIA Label Error</span></span>

## <a name="text"></a><span data-ttu-id="6cf51-105">Texto</span><span class="sxs-lookup"><span data-stu-id="6cf51-105">Text</span></span>

<span data-ttu-id="6cf51-106">O elemento é do tipo **entrada**, **botão**, **imagem-botão** ou **ponto de referência** , mas não tem um nome acessível.</span><span class="sxs-lookup"><span data-stu-id="6cf51-106">Element is of type **input**, **button**, **image-button** or **landmark** but doesn't have an accessible name.</span></span>

## <a name="type"></a><span data-ttu-id="6cf51-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6cf51-107">Type</span></span>

<span data-ttu-id="6cf51-108">Erro</span><span class="sxs-lookup"><span data-stu-id="6cf51-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="6cf51-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cf51-109">Description</span></span>

<span data-ttu-id="6cf51-110">Este erro se aplica a:</span><span class="sxs-lookup"><span data-stu-id="6cf51-110">This error applies to:</span></span>

-   <span data-ttu-id="6cf51-111">Campos de entrada de formulário:</span><span class="sxs-lookup"><span data-stu-id="6cf51-111">Form input fields:</span></span>
    -   <span data-ttu-id="6cf51-112">Marcas HTML —**tipo de entrada \[ = " \| caixa de seleção de senha de texto arquivo de \| \| rádio \| \| \| telefone \| de cor do Tel \| Data \| DateTime \| DateTime-local \| \| semana hora \| mês \| número intervalo de \| \| pesquisa \| URL \] "**, **Select**, **DataList** e **TextArea**.</span><span class="sxs-lookup"><span data-stu-id="6cf51-112">HTML tags—**input\[type= "text\|password\|checkbox\|radio\|file\|email\|tel\|color\|date\|datetime\|datetime-local\|time\|week\|month\|number\|range\|search\|url"\]**, **select**, **datalist**, and **textarea**.</span></span>
    -   <span data-ttu-id="6cf51-113">WAI-funções do ARIA —**CheckBox**, **ComboBox**, ListBox **, Radiogroup,**  **Radio**, **TextBox**, **Tree**, **Slider** e **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="6cf51-113">WAI-ARIA roles—**checkbox**, **combobox**, **listbox**, **radiogroup**, **radio**, **textbox**, **tree**, **slider**, and **spinbutton**.</span></span>
-   <span data-ttu-id="6cf51-114">Imagens/botões/botões de imagem</span><span class="sxs-lookup"><span data-stu-id="6cf51-114">Images/image buttons/ buttons</span></span>
    -   <span data-ttu-id="6cf51-115">Marcas HTML —**img**, **Input \[ Type = "Image \| Button" \]** e **Button**.</span><span class="sxs-lookup"><span data-stu-id="6cf51-115">HTML tags—**img**, **input\[type="image\|button"\]**, and **button**.</span></span>
    -   <span data-ttu-id="6cf51-116">WAI-funções do ARIA —**img** e **Button**.</span><span class="sxs-lookup"><span data-stu-id="6cf51-116">WAI-ARIA roles—**img** and **button**.</span></span>
-   <span data-ttu-id="6cf51-117">Pontos de referência</span><span class="sxs-lookup"><span data-stu-id="6cf51-117">Landmarks</span></span>
    -   <span data-ttu-id="6cf51-118">WAI-funções do ARIA —**região**, **faixa**, **complementar**, **ContentInfo**, **formulário**, **principal**, **navegação** e **pesquisa**.</span><span class="sxs-lookup"><span data-stu-id="6cf51-118">WAI-ARIA roles—**region**, **banner**, **complementary**, **contentinfo**, **form**, **main**, **navigation**, and **search**.</span></span>

> [!Note]  
> <span data-ttu-id="6cf51-119">AccChecker mostra esse erro até mesmo para elementos para os quais o nome acessível é definido por padrão com base no conteúdo HTML interno (consulte o elemento **banner** no exemplo acima).</span><span class="sxs-lookup"><span data-stu-id="6cf51-119">AccChecker shows this error even for elements for which the accessible name is set by default based on inner HTML content (see the **banner** element in the above example).</span></span> <span data-ttu-id="6cf51-120">Nesses casos, você pode suprimir esses erros.</span><span class="sxs-lookup"><span data-stu-id="6cf51-120">For these cases, you can suppress this errors.</span></span>

 

<span data-ttu-id="6cf51-121">Todos os elementos de interface do usuário semanticamente importantes, como campos de formulário (por exemplo, **entrada**, **seleção**, **TextArea**), imagens, botões e pontos de referência (marcas que representam regiões lógicas) devem ter o nome acessível para permitir que os leitores de tela os anunciem corretamente.</span><span class="sxs-lookup"><span data-stu-id="6cf51-121">All semantically important UI elements such as form fields (for example, **input**, **select**, **textarea**), images, buttons and landmarks (tags representing logical regions) must have the accessible name to allow screen readers to correctly announce them.</span></span>

<span data-ttu-id="6cf51-122">Para corrigir esse erro, defina o nome acessível de uma das seguintes maneiras (listadas na ordem de preferência).</span><span class="sxs-lookup"><span data-stu-id="6cf51-122">To fix this error, set the accessible name in one of the following ways (listed in the order of preference).</span></span>

-   <span data-ttu-id="6cf51-123">Campos de formulário: Use a marca de **rótulo** e defina o atributo **para** como o valor de **ID** do campo de destino.</span><span class="sxs-lookup"><span data-stu-id="6cf51-123">Form fields: Use the **label** tag and set the **for** attribute to the **id** value of the target field.</span></span>
-   <span data-ttu-id="6cf51-124">Botão de imagem/imagem: defina o atributo **ALT** .</span><span class="sxs-lookup"><span data-stu-id="6cf51-124">Image/image button: Set the **alt** attribute.</span></span>
-   <span data-ttu-id="6cf51-125">Botões: defina o texto da legenda do botão.</span><span class="sxs-lookup"><span data-stu-id="6cf51-125">Buttons: Set the button caption text.</span></span>
-   <span data-ttu-id="6cf51-126">Para qualquer elemento:</span><span class="sxs-lookup"><span data-stu-id="6cf51-126">For any element:</span></span>
    -   <span data-ttu-id="6cf51-127">atributo [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : Defina como o valor de **ID** do elemento que contém a cadeia de caracteres de nome acessível.</span><span class="sxs-lookup"><span data-stu-id="6cf51-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the **id** value of the element containing the accessible name string.</span></span>
    -   <span data-ttu-id="6cf51-128">atributo [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : definido como a cadeia de caracteres de nome acessível.</span><span class="sxs-lookup"><span data-stu-id="6cf51-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the accessible name string.</span></span>
    -   <span data-ttu-id="6cf51-129">atributo de [**título**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : Defina como a cadeia de caracteres de nome acessível (também crie uma **dica de ferramenta**).</span><span class="sxs-lookup"><span data-stu-id="6cf51-129">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attribute: Set to the accessible name string (also create a **tooltip**).</span></span>

## <a name="example"></a><span data-ttu-id="6cf51-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6cf51-130">Example</span></span>


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



 

 




