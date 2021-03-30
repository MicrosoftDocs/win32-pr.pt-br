---
description: A tabela de propriedades contém os nomes e valores de propriedade de todas as propriedades definidas na instalação. Propriedades com valores nulos não estão presentes na tabela.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Tabela de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662149"
---
# <a name="property-table"></a><span data-ttu-id="61220-104">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="61220-104">Property Table</span></span>

<span data-ttu-id="61220-105">A tabela de propriedades contém os nomes e valores de propriedade de todas as propriedades definidas na instalação.</span><span class="sxs-lookup"><span data-stu-id="61220-105">The Property table contains the property names and values for all defined properties in the installation.</span></span> <span data-ttu-id="61220-106">Propriedades com valores nulos não estão presentes na tabela.</span><span class="sxs-lookup"><span data-stu-id="61220-106">Properties with Null values are not present in the table.</span></span>

<span data-ttu-id="61220-107">A tabela de propriedades tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="61220-107">The Property table has the following columns.</span></span>



| <span data-ttu-id="61220-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="61220-108">Column</span></span>   | <span data-ttu-id="61220-109">Type</span><span class="sxs-lookup"><span data-stu-id="61220-109">Type</span></span>                         | <span data-ttu-id="61220-110">Chave</span><span class="sxs-lookup"><span data-stu-id="61220-110">Key</span></span> | <span data-ttu-id="61220-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="61220-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="61220-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="61220-112">Property</span></span> | [<span data-ttu-id="61220-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="61220-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="61220-114">S</span><span class="sxs-lookup"><span data-stu-id="61220-114">Y</span></span>   | <span data-ttu-id="61220-115">N</span><span class="sxs-lookup"><span data-stu-id="61220-115">N</span></span>        |
| <span data-ttu-id="61220-116">Valor</span><span class="sxs-lookup"><span data-stu-id="61220-116">Value</span></span>    | [<span data-ttu-id="61220-117">Text</span><span class="sxs-lookup"><span data-stu-id="61220-117">Text</span></span>](text.md)             | <span data-ttu-id="61220-118">N</span><span class="sxs-lookup"><span data-stu-id="61220-118">N</span></span>   | <span data-ttu-id="61220-119">N</span><span class="sxs-lookup"><span data-stu-id="61220-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="61220-120">Colunas</span><span class="sxs-lookup"><span data-stu-id="61220-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="61220-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade</span><span class="sxs-lookup"><span data-stu-id="61220-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="61220-122">O nome de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="61220-122">The name of a property.</span></span> <span data-ttu-id="61220-123">Consulte [Propriedades](properties.md).</span><span class="sxs-lookup"><span data-stu-id="61220-123">See [Properties](properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="61220-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="61220-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="61220-125">Um valor de cadeia de caracteres localizável para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="61220-125">A localizable string value for the property.</span></span> <span data-ttu-id="61220-126">Isso pode nunca ser nulo ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="61220-126">This may never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61220-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="61220-127">Remarks</span></span>

<span data-ttu-id="61220-128">Observe que você não pode usar a tabela de propriedades para definir uma propriedade para o valor de outra propriedade.</span><span class="sxs-lookup"><span data-stu-id="61220-128">Note that you cannot use the Property table to set a property to the value of another property.</span></span> <span data-ttu-id="61220-129">O instalador não faz nada para a cadeia de caracteres de texto inserida na coluna valor antes de definir a propriedade na coluna propriedade.</span><span class="sxs-lookup"><span data-stu-id="61220-129">The installer does nothing to the text string entered in the Value column before setting the property in the Property column.</span></span> <span data-ttu-id="61220-130">Se Firstproperty for inserido na coluna de propriedade e \[ segundoproperty \] na coluna Value, o valor de firstproperty será definido como a cadeia de texto " \[ secondproperty \] " e não com o valor da propriedade segundaproperty.</span><span class="sxs-lookup"><span data-stu-id="61220-130">If FirstProperty is entered into the Property column and \[SecondProperty\] in the Value column, the value of FirstProperty is set to the text string "\[SecondProperty\]" and not to the value of the SecondProperty property.</span></span> <span data-ttu-id="61220-131">Isso é necessário para evitar a criação de referências circulares na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="61220-131">This is necessary to prevent creating circular references in the Property table.</span></span> <span data-ttu-id="61220-132">Em vez disso, você pode definir uma propriedade para outra usando um [tipo de ação personalizada 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="61220-132">Instead, you can set one property to another by using a [Custom Action Type 51](custom-action-type-51.md).</span></span>

<span data-ttu-id="61220-133">Observe que a propriedade [**adminproperties**](adminproperties.md) pode ser usada para substituir os valores na tabela de propriedades durante uma [instalação administrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="61220-133">Note that the [**AdminProperties**](adminproperties.md) property can be used to override the values in the Property table during an [Administrative Installation](administrative-installation.md).</span></span>

<span data-ttu-id="61220-134">Não use Propriedades para senhas ou outras informações que devam permanecer seguras.</span><span class="sxs-lookup"><span data-stu-id="61220-134">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="61220-135">O instalador pode gravar o valor de uma propriedade criada na tabela de propriedades ou criado em tempo de execução, em um log ou no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="61220-135">The installer may write the value of a property authored into the Property table, or created at runtime, into a log or the system registry.</span></span>

## <a name="validation"></a><span data-ttu-id="61220-136">Validação</span><span class="sxs-lookup"><span data-stu-id="61220-136">Validation</span></span>

<dl>

[<span data-ttu-id="61220-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="61220-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="61220-138">ICE05</span><span class="sxs-lookup"><span data-stu-id="61220-138">ICE05</span></span>](ice05.md)  
[<span data-ttu-id="61220-139">ICE06</span><span class="sxs-lookup"><span data-stu-id="61220-139">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="61220-140">ICE16</span><span class="sxs-lookup"><span data-stu-id="61220-140">ICE16</span></span>](ice16.md)  
[<span data-ttu-id="61220-141">ICE24</span><span class="sxs-lookup"><span data-stu-id="61220-141">ICE24</span></span>](ice24.md)  
[<span data-ttu-id="61220-142">ICE31</span><span class="sxs-lookup"><span data-stu-id="61220-142">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="61220-143">ICE34</span><span class="sxs-lookup"><span data-stu-id="61220-143">ICE34</span></span>](ice34.md)  
[<span data-ttu-id="61220-144">ICE36</span><span class="sxs-lookup"><span data-stu-id="61220-144">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="61220-145">ICE40</span><span class="sxs-lookup"><span data-stu-id="61220-145">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="61220-146">ICE46</span><span class="sxs-lookup"><span data-stu-id="61220-146">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="61220-147">ICE48</span><span class="sxs-lookup"><span data-stu-id="61220-147">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="61220-148">ICE52</span><span class="sxs-lookup"><span data-stu-id="61220-148">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="61220-149">ICE61</span><span class="sxs-lookup"><span data-stu-id="61220-149">ICE61</span></span>](ice61.md)  
[<span data-ttu-id="61220-150">ICE73</span><span class="sxs-lookup"><span data-stu-id="61220-150">ICE73</span></span>](ice73.md)  
[<span data-ttu-id="61220-151">ICE74</span><span class="sxs-lookup"><span data-stu-id="61220-151">ICE74</span></span>](ice74.md)  
[<span data-ttu-id="61220-152">ICE80</span><span class="sxs-lookup"><span data-stu-id="61220-152">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="61220-153">ICE87</span><span class="sxs-lookup"><span data-stu-id="61220-153">ICE87</span></span>](ice87.md)  
[<span data-ttu-id="61220-154">ICE88</span><span class="sxs-lookup"><span data-stu-id="61220-154">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="61220-155">ICE91</span><span class="sxs-lookup"><span data-stu-id="61220-155">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="61220-156">ICE99</span><span class="sxs-lookup"><span data-stu-id="61220-156">ICE99</span></span>](ice99.md)  
</dl>

 

 



