---
description: É o elemento raiz de um arquivo de script XML do gerador de código WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: elemento wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812327"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="cd1fc-103">elemento wsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="cd1fc-103">wsdCodeGen element</span></span>

<span data-ttu-id="cd1fc-104">É o elemento raiz de um arquivo de script XML do gerador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="cd1fc-105">Uso</span><span class="sxs-lookup"><span data-stu-id="cd1fc-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="cd1fc-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="cd1fc-106">Attributes</span></span>



| <span data-ttu-id="cd1fc-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="cd1fc-107">Attribute</span></span>                        | <span data-ttu-id="cd1fc-108">Type</span><span class="sxs-lookup"><span data-stu-id="cd1fc-108">Type</span></span>                             | <span data-ttu-id="cd1fc-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cd1fc-109">Required</span></span>       | <span data-ttu-id="cd1fc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd1fc-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd1fc-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="cd1fc-112">Qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-112">Any character string.</span></span><br/> | <span data-ttu-id="cd1fc-113">Yes</span><span class="sxs-lookup"><span data-stu-id="cd1fc-113">Yes</span></span><br/> | <span data-ttu-id="cd1fc-114">A versão do arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-114">The version of the configuration file.</span></span> <span data-ttu-id="cd1fc-115">O único valor válido é "1,0".</span><span class="sxs-lookup"><span data-stu-id="cd1fc-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="cd1fc-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cd1fc-116">Child elements</span></span>



| <span data-ttu-id="cd1fc-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="cd1fc-117">Element</span></span>                                                         | <span data-ttu-id="cd1fc-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd1fc-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd1fc-119">**autoestático**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="cd1fc-120">Indica se WsdCodeGen deve tentar sinalizar automaticamente determinados campos gerados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="cd1fc-121">Isso é habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="cd1fc-122">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="cd1fc-123">Direciona o gerador de código para gerar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="cd1fc-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="cd1fc-125">Os metadados de hospedagem para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="cd1fc-126">Este elemento é usado apenas para implementações de dispositivo (hosts).</span><span class="sxs-lookup"><span data-stu-id="cd1fc-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="cd1fc-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="cd1fc-128">O número da camada de código a ser gerada.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="cd1fc-129">Os números de camada são usados em tabelas de tempo de execução para distinguir uma camada de código para outra.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="cd1fc-130">O WSDAPI usa o código gerado que tem um número de camada de 0.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="cd1fc-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="cd1fc-132">O prefixo a ser usado no código gerado para garantir a exclusividade dos símbolos gerados.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="cd1fc-133">O WSDAPI usa o prefixo "WSD".</span><span class="sxs-lookup"><span data-stu-id="cd1fc-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="cd1fc-134">**Ela**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="cd1fc-135">Define o texto ou CDATA a ser reutilizado pelo elemento [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="cd1fc-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="cd1fc-136">**nameSpace**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="cd1fc-137">Descreve um namespace a ser usado para geração de código.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="cd1fc-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="cd1fc-139">Descreve o host e os metadados hospedados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="cd1fc-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="cd1fc-141">Os metadados de modelo e fabricante para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="cd1fc-142">Este elemento é usado apenas para implementações de dispositivo (hosts).</span><span class="sxs-lookup"><span data-stu-id="cd1fc-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="cd1fc-143">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="cd1fc-144">Especifica um arquivo WSDL para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="cd1fc-145">**XSD**</span><span class="sxs-lookup"><span data-stu-id="cd1fc-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="cd1fc-146">Especifica um arquivo XSD para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="cd1fc-147">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="cd1fc-147">Child element sequence</span></span>

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a><span data-ttu-id="cd1fc-148">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cd1fc-148">Parent elements</span></span>

<span data-ttu-id="cd1fc-149">Não há elementos pai.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd1fc-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd1fc-150">Remarks</span></span>

<span data-ttu-id="cd1fc-151">Em geral, os elementos de [**arquivo**](file.md) devem ocorrer por último porque geram código que usa os dados especificados pelos outros elementos.</span><span class="sxs-lookup"><span data-stu-id="cd1fc-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="cd1fc-152">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cd1fc-152">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="cd1fc-153">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd1fc-153">Minimum supported system</span></span><br/> | <span data-ttu-id="cd1fc-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd1fc-154">Windows Vista</span></span> |
| <span data-ttu-id="cd1fc-155">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="cd1fc-155">Can be empty</span></span>                        | <span data-ttu-id="cd1fc-156">Sim</span><span class="sxs-lookup"><span data-stu-id="cd1fc-156">Yes</span></span>           |



 

 




