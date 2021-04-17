---
title: Elemento QuickAccessToolbar
description: Representa a barra de ferramentas de acesso rápido (QAT), uma pequena barra de ferramentas que exibe atalhos para comandos da faixa de das faixas.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Faixa de QuickAccessToolbar do elemento do Windows
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365497"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="ea4f5-104">Elemento QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="ea4f5-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="ea4f5-105">Representa a [barra de ferramentas de acesso rápido (qat)](windowsribbon-controls-quickaccesstoolbar.md), uma pequena barra de ferramentas que exibe atalhos para comandos da faixa de das faixas.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="ea4f5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ea4f5-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="ea4f5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ea4f5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea4f5-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea4f5-108">Attribute</span></span></th>
<th><span data-ttu-id="ea4f5-109">Type</span><span class="sxs-lookup"><span data-stu-id="ea4f5-109">Type</span></span></th>
<th><span data-ttu-id="ea4f5-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ea4f5-110">Required</span></span></th>
<th><span data-ttu-id="ea4f5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea4f5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea4f5-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ea4f5-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ea4f5-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="ea4f5-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ea4f5-114">Não</span><span class="sxs-lookup"><span data-stu-id="ea4f5-114">No</span></span><br/></td>
<td><span data-ttu-id="ea4f5-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ea4f5-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="ea4f5-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ea4f5-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ea4f5-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ea4f5-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea4f5-120"><strong>CustomizeCommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ea4f5-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ea4f5-121">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="ea4f5-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ea4f5-122">Não</span><span class="sxs-lookup"><span data-stu-id="ea4f5-122">No</span></span><br/></td>
<td><span data-ttu-id="ea4f5-123">Insere um item de comando adicional no menu QAT.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="ea4f5-124">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="ea4f5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="ea4f5-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ea4f5-126">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ea4f5-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ea4f5-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ea4f5-128">Child elements</span></span>



| <span data-ttu-id="ea4f5-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea4f5-129">Element</span></span>                                                                                                                   | <span data-ttu-id="ea4f5-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea4f5-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ea4f5-131">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="ea4f5-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="ea4f5-132">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="ea4f5-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ea4f5-133">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ea4f5-133">Parent elements</span></span>



| <span data-ttu-id="ea4f5-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea4f5-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea4f5-135">**Ribbon. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="ea4f5-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ea4f5-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea4f5-136">Remarks</span></span>

<span data-ttu-id="ea4f5-137">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-137">Required.</span></span>

<span data-ttu-id="ea4f5-138">Deve ocorrer exatamente uma vez para cada [**Ribbon. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="ea4f5-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="ea4f5-139">Os itens no QAT podem ser adicionados ou removidos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="ea4f5-140">Para fins de consistência em aplicativos de faixa de faixas, é recomendável que o manipulador de comandos *CustomizeCommandName* inicie uma caixa de diálogo de personalização qat.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="ea4f5-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ea4f5-141">Examples</span></span>

<span data-ttu-id="ea4f5-142">O exemplo a seguir demonstra a marcação básica para o **QuickAccessToolbar**.</span><span class="sxs-lookup"><span data-stu-id="ea4f5-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="ea4f5-143">Esta seção de código mostra a declaração de comando **QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="ea4f5-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="ea4f5-144">Esta seção de código mostra a declaração de controle **QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="ea4f5-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="ea4f5-145">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ea4f5-145">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ea4f5-146">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea4f5-146">Minimum supported system</span></span><br/> | <span data-ttu-id="ea4f5-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea4f5-147">Windows 7</span></span> |
| <span data-ttu-id="ea4f5-148">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="ea4f5-148">Can be empty</span></span>                        | <span data-ttu-id="ea4f5-149">Não</span><span class="sxs-lookup"><span data-stu-id="ea4f5-149">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="ea4f5-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea4f5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4f5-151">Controle da barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="ea4f5-151">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





