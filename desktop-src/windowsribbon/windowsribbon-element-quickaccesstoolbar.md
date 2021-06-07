---
title: Elemento QuickAccessToolbar
description: Representa a QAT (Barra de Ferramentas de Acesso Rápido), uma pequena barra de ferramentas que exibe atalhos para Comandos da Faixa de Opções.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Faixa de Opções do Windows do elemento QuickAccessToolbar
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae01f620d66298a5f7200d0be947dbfb3750af4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443297"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="0bef5-104">Elemento QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="0bef5-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="0bef5-105">Representa a [QAT (Barra](windowsribbon-controls-quickaccesstoolbar.md)de Ferramentas de Acesso Rápido), uma pequena barra de ferramentas que exibe atalhos para Comandos da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="0bef5-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="0bef5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="0bef5-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="0bef5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0bef5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0bef5-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="0bef5-108">Attribute</span></span></th>
<th><span data-ttu-id="0bef5-109">Type</span><span class="sxs-lookup"><span data-stu-id="0bef5-109">Type</span></span></th>
<th><span data-ttu-id="0bef5-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0bef5-110">Required</span></span></th>
<th><span data-ttu-id="0bef5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bef5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bef5-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="0bef5-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="0bef5-113">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="0bef5-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0bef5-114">Não</span><span class="sxs-lookup"><span data-stu-id="0bef5-114">No</span></span><br/></td>
<td><span data-ttu-id="0bef5-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0bef5-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="0bef5-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="0bef5-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0bef5-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="0bef5-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="0bef5-118">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="0bef5-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="0bef5-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0bef5-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bef5-120"><strong>CustomizeCommandName</strong></span><span class="sxs-lookup"><span data-stu-id="0bef5-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="0bef5-121">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="0bef5-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0bef5-122">Não</span><span class="sxs-lookup"><span data-stu-id="0bef5-122">No</span></span><br/></td>
<td><span data-ttu-id="0bef5-123">Insere um item command adicional no menu QAT.</span><span class="sxs-lookup"><span data-stu-id="0bef5-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="0bef5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="0bef5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="0bef5-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="0bef5-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="0bef5-126">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="0bef5-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="0bef5-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0bef5-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0bef5-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0bef5-128">Child elements</span></span>



| <span data-ttu-id="0bef5-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="0bef5-129">Element</span></span>                                                                                                                   | <span data-ttu-id="0bef5-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bef5-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="0bef5-131">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="0bef5-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="0bef5-132">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="0bef5-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0bef5-133">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0bef5-133">Parent elements</span></span>



| <span data-ttu-id="0bef5-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="0bef5-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bef5-135">**Ribbon.QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="0bef5-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0bef5-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bef5-136">Remarks</span></span>

<span data-ttu-id="0bef5-137">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0bef5-137">Required.</span></span>

<span data-ttu-id="0bef5-138">Deve ocorrer exatamente uma vez para cada [**Ribbon.QuickAccessToolbar.**](windowsribbon-element-ribbon-quickaccesstoolbar.md)</span><span class="sxs-lookup"><span data-stu-id="0bef5-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="0bef5-139">Os itens no QAT podem ser adicionados ou removidos em tempo de executar.</span><span class="sxs-lookup"><span data-stu-id="0bef5-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="0bef5-140">Para consistência entre aplicativos de Faixa de Opções, é recomendável que o manipulador de comandos *CustomizeCommandName* iniciar uma caixa de diálogo de personalização de QAT.</span><span class="sxs-lookup"><span data-stu-id="0bef5-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="0bef5-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0bef5-141">Examples</span></span>

<span data-ttu-id="0bef5-142">O exemplo a seguir demonstra a marcação básica para **o QuickAccessToolbar**.</span><span class="sxs-lookup"><span data-stu-id="0bef5-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="0bef5-143">Esta seção de código mostra a **declaração comando QuickAccessToolbar.**</span><span class="sxs-lookup"><span data-stu-id="0bef5-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="0bef5-144">Esta seção de código mostra a **declaração de controle QuickAccessToolbar.**</span><span class="sxs-lookup"><span data-stu-id="0bef5-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="0bef5-145">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0bef5-145">Element information</span></span>

* <span data-ttu-id="0bef5-146">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="0bef5-146">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="0bef5-147">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="0bef5-147">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="0bef5-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bef5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bef5-149">Controle da Barra de Ferramentas de Acesso Rápido</span><span class="sxs-lookup"><span data-stu-id="0bef5-149">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





