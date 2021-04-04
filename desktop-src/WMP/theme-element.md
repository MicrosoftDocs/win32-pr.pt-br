---
title: Elemento THEME
description: Elemento THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Capas do Windows Media Player, elemento THEME
- capas, elemento THEME
- Elemento THEME
- referência para capas, elemento THEME
- elementos, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822440"
---
# <a name="theme-element"></a><span data-ttu-id="701ff-108">Elemento THEME</span><span class="sxs-lookup"><span data-stu-id="701ff-108">THEME Element</span></span>

<span data-ttu-id="701ff-109">O elemento **Theme** é o elemento de nível pai de uma capa e contém um ou mais elementos **View** que, por sua vez, contêm todos os outros elementos em uma capa.</span><span class="sxs-lookup"><span data-stu-id="701ff-109">The **THEME** element is the parent-level element of a skin, and contains one or more **VIEW** elements, which in turn contain all other elements within a skin.</span></span> <span data-ttu-id="701ff-110">No código do script, o elemento **Theme** é acessado por meio do atributo global **Theme** , em vez de um nome especificado por um atributo **ID** , que não tem suporte do elemento **Theme** .</span><span class="sxs-lookup"><span data-stu-id="701ff-110">Within script code, the **THEME** element is accessed through the **theme** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **THEME** element.</span></span>

<span data-ttu-id="701ff-111">O elemento **Theme** dá suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="701ff-111">The **THEME** element supports the following attributes.</span></span>



| <span data-ttu-id="701ff-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="701ff-112">Attribute</span></span>                                | <span data-ttu-id="701ff-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="701ff-113">Description</span></span>                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="701ff-114">autorização</span><span class="sxs-lookup"><span data-stu-id="701ff-114">author</span></span>](theme-author.md)               | <span data-ttu-id="701ff-115">Especifica ou recupera o nome do autor da capa.</span><span class="sxs-lookup"><span data-stu-id="701ff-115">Specifies or retrieves the name of the author of the skin.</span></span>                                                                      |
| [<span data-ttu-id="701ff-116">authorVersion</span><span class="sxs-lookup"><span data-stu-id="701ff-116">authorVersion</span></span>](theme-authorversion.md) | <span data-ttu-id="701ff-117">Especifica ou recupera o número de versão da capa, conforme atribuído pelo autor.</span><span class="sxs-lookup"><span data-stu-id="701ff-117">Specifies or retrieves the version number of the skin as assigned by the author.</span></span>                                                |
| [<span data-ttu-id="701ff-118">internacionais</span><span class="sxs-lookup"><span data-stu-id="701ff-118">copyright</span></span>](theme-copyright.md)         | <span data-ttu-id="701ff-119">Especifica ou recupera a cadeia de caracteres de direitos autorais para a capa.</span><span class="sxs-lookup"><span data-stu-id="701ff-119">Specifies or retrieves the copyright string for the skin.</span></span>                                                                       |
| [<span data-ttu-id="701ff-120">currentViewID</span><span class="sxs-lookup"><span data-stu-id="701ff-120">currentViewID</span></span>](theme-currentviewid.md) | <span data-ttu-id="701ff-121">Especifica ou recupera a **exibição** exibida no momento.</span><span class="sxs-lookup"><span data-stu-id="701ff-121">Specifies or retrieves the currently displayed **VIEW**.</span></span>                                                                        |
| [<span data-ttu-id="701ff-122">title</span><span class="sxs-lookup"><span data-stu-id="701ff-122">title</span></span>](theme-title.md)                 | <span data-ttu-id="701ff-123">Especifica ou recupera o título da capa.</span><span class="sxs-lookup"><span data-stu-id="701ff-123">Specifies or retrieves the title of the skin.</span></span>                                                                                   |
| [<span data-ttu-id="701ff-124">version</span><span class="sxs-lookup"><span data-stu-id="701ff-124">version</span></span>](theme-version.md)             | <span data-ttu-id="701ff-125">Especifica ou recupera o número de versão do Windows Media Player para o qual a capa foi criada.</span><span class="sxs-lookup"><span data-stu-id="701ff-125">Specifies or retrieves the Windows Media Player version number for which the skin was authored.</span></span> <span data-ttu-id="701ff-126">Só pode ser definido em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="701ff-126">Can only be set at design time.</span></span> |



 

<span data-ttu-id="701ff-127">O elemento **Theme** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="701ff-127">The **THEME** element supports the following methods.</span></span>



| <span data-ttu-id="701ff-128">Método</span><span class="sxs-lookup"><span data-stu-id="701ff-128">Method</span></span>                                         | <span data-ttu-id="701ff-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="701ff-129">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="701ff-130">closeView</span><span class="sxs-lookup"><span data-stu-id="701ff-130">closeView</span></span>](theme-closeview.md)               | <span data-ttu-id="701ff-131">Fecha um **modo de exibição** aberto.</span><span class="sxs-lookup"><span data-stu-id="701ff-131">Closes an open **VIEW**.</span></span>                                                                                        |
| [<span data-ttu-id="701ff-132">loadpreference</span><span class="sxs-lookup"><span data-stu-id="701ff-132">loadPreference</span></span>](theme-loadpreference.md)     | <span data-ttu-id="701ff-133">Carrega uma preferência do registro.</span><span class="sxs-lookup"><span data-stu-id="701ff-133">Loads a preference from the registry.</span></span>                                                                           |
| [<span data-ttu-id="701ff-134">logString</span><span class="sxs-lookup"><span data-stu-id="701ff-134">logString</span></span>](theme-logstring.md)               | <span data-ttu-id="701ff-135">Registra uma cadeia de caracteres definida pelo usuário no arquivo de erro, se o registro em log estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="701ff-135">Logs a user-defined string to the error file, if logging is enabled.</span></span>                                            |
| [<span data-ttu-id="701ff-136">openDialog</span><span class="sxs-lookup"><span data-stu-id="701ff-136">openDialog</span></span>](theme-opendialog.md)             | <span data-ttu-id="701ff-137">Abre uma caixa de diálogo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="701ff-137">Opens a file dialog box.</span></span>                                                                                        |
| [<span data-ttu-id="701ff-138">AbrirModoDeExibição</span><span class="sxs-lookup"><span data-stu-id="701ff-138">openView</span></span>](theme-openview.md)                 | <span data-ttu-id="701ff-139">Abre uma **exibição** em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="701ff-139">Opens a **VIEW** in a new window.</span></span>                                                                               |
| [<span data-ttu-id="701ff-140">openViewRelative</span><span class="sxs-lookup"><span data-stu-id="701ff-140">openViewRelative</span></span>](theme-openviewrelative.md) | <span data-ttu-id="701ff-141">Abre uma **exibição** em uma nova janela em uma posição inicial especificada em relação ao canto superior esquerdo da capa.</span><span class="sxs-lookup"><span data-stu-id="701ff-141">Opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span> |
| [<span data-ttu-id="701ff-142">playSound</span><span class="sxs-lookup"><span data-stu-id="701ff-142">playSound</span></span>](theme-playsound.md)               | <span data-ttu-id="701ff-143">Reproduz o arquivo de som especificado.</span><span class="sxs-lookup"><span data-stu-id="701ff-143">Plays the specified sound file.</span></span>                                                                                 |
| [<span data-ttu-id="701ff-144">savePreference</span><span class="sxs-lookup"><span data-stu-id="701ff-144">savePreference</span></span>](theme-savepreference.md)     | <span data-ttu-id="701ff-145">Salva uma preferência no registro.</span><span class="sxs-lookup"><span data-stu-id="701ff-145">Saves a preference in the registry.</span></span>                                                                             |
| [<span data-ttu-id="701ff-146">showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="701ff-146">showErrorDialog</span></span>](theme-showerrordialog.md)   | <span data-ttu-id="701ff-147">Exibe a caixa de diálogo de erro padrão.</span><span class="sxs-lookup"><span data-stu-id="701ff-147">Displays the standard error dialog box.</span></span>                                                                         |



 

<span data-ttu-id="701ff-148">O elemento **Theme** não dá suporte a manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="701ff-148">The **THEME** element does not support event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="701ff-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="701ff-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="701ff-150">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="701ff-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




