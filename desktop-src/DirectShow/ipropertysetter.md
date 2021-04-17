---
description: 'A interface IPropertySetter define propriedades em um efeito ou transição nos serviços de edição do DirectShow (DES). Para usar essa interface, crie uma instância de um objeto setter de propriedade (CLSID \_ PropertySetter) e associe-o a um efeito ou transição chamando o método IAMTimelineObj:: SetPropertySetter. Para obter mais informações, consulte trabalhando com efeitos e transições. geralmente um aplicativo precisa chamar apenas o método IPropertySetter:: ClearProps para limpar as propriedades existentes e o método IPropertySetter:: addprop para adicionar novas propriedades. Os outros métodos nessa interface são chamados por outros componentes DES.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interface IPropertySetter (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759534"
---
# <a name="ipropertysetter-interface"></a><span data-ttu-id="68fc4-105">Interface IPropertySetter</span><span class="sxs-lookup"><span data-stu-id="68fc4-105">IPropertySetter interface</span></span>

> [!Note]  
> <span data-ttu-id="68fc4-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="68fc4-106">\[Deprecated.</span></span> <span data-ttu-id="68fc4-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="68fc4-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="68fc4-108">A `IPropertySetter` interface define as propriedades em um efeito ou uma transição nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="68fc4-108">The `IPropertySetter` interface sets properties on an effect or transition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="68fc4-109">Para usar essa interface, crie uma instância de um objeto setter de propriedade (CLSID \_ PropertySetter) e associe-o a um efeito ou transição chamando o método [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="68fc4-109">To use this interface, create an instance of a property setter object (CLSID\_PropertySetter), and associate it with an effect or transition by calling the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span> <span data-ttu-id="68fc4-110">Para obter mais informações, consulte [trabalhando com efeitos e transições](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="68fc4-110">For more information, see [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

<span data-ttu-id="68fc4-111">Normalmente, um aplicativo precisa chamar apenas o método [**IPropertySetter:: ClearProps**](ipropertysetter-clearprops.md) para limpar as propriedades existentes e o método [**IPropertySetter:: addprop**](ipropertysetter-addprop.md) para adicionar novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="68fc4-111">Usually an application needs to call only the [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) method to clear existing properties, and the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method to add new properties.</span></span> <span data-ttu-id="68fc4-112">Os outros métodos nessa interface são chamados por outros componentes DES.</span><span class="sxs-lookup"><span data-stu-id="68fc4-112">The other methods on this interface are called by other DES components.</span></span>

## <a name="members"></a><span data-ttu-id="68fc4-113">Membros</span><span class="sxs-lookup"><span data-stu-id="68fc4-113">Members</span></span>

<span data-ttu-id="68fc4-114">A interface **IPropertySetter** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="68fc4-114">The **IPropertySetter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="68fc4-115">**IPropertySetter** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68fc4-115">**IPropertySetter** also has these types of members:</span></span>

-   [<span data-ttu-id="68fc4-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="68fc4-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="68fc4-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="68fc4-117">Methods</span></span>

<span data-ttu-id="68fc4-118">A interface **IPropertySetter** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="68fc4-118">The **IPropertySetter** interface has these methods.</span></span>



| <span data-ttu-id="68fc4-119">Método</span><span class="sxs-lookup"><span data-stu-id="68fc4-119">Method</span></span>                                               | <span data-ttu-id="68fc4-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="68fc4-120">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68fc4-121">**Addprop**</span><span class="sxs-lookup"><span data-stu-id="68fc4-121">**AddProp**</span></span>](ipropertysetter-addprop.md)           | <span data-ttu-id="68fc4-122">Adiciona uma propriedade ao setter de propriedade, com uma matriz de pares time-Value que definem o valor da propriedade em um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="68fc4-122">Adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span><br/> |
| [<span data-ttu-id="68fc4-123">**ClearProps**</span><span class="sxs-lookup"><span data-stu-id="68fc4-123">**ClearProps**</span></span>](ipropertysetter-clearprops.md)     | <span data-ttu-id="68fc4-124">Limpa todos os dados de Propriedade do setter de propriedade.</span><span class="sxs-lookup"><span data-stu-id="68fc4-124">Clears all property data from the property setter.</span></span><br/>                                                                                 |
| [<span data-ttu-id="68fc4-125">**CloneProps**</span><span class="sxs-lookup"><span data-stu-id="68fc4-125">**CloneProps**</span></span>](ipropertysetter-cloneprops.md)     | <span data-ttu-id="68fc4-126">Clona um conjunto de propriedades desse setter de propriedade e as adiciona a um novo setter de propriedade.</span><span class="sxs-lookup"><span data-stu-id="68fc4-126">Clones a set of properties from this property setter and adds them to a new property setter.</span></span><br/>                                       |
| [<span data-ttu-id="68fc4-127">**FreeProps**</span><span class="sxs-lookup"><span data-stu-id="68fc4-127">**FreeProps**</span></span>](ipropertysetter-freeprops.md)       | <span data-ttu-id="68fc4-128">Libera recursos alocados pelo método [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="68fc4-128">Frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span><br/>                             |
| [<span data-ttu-id="68fc4-129">**GetProps**</span><span class="sxs-lookup"><span data-stu-id="68fc4-129">**GetProps**</span></span>](ipropertysetter-getprops.md)         | <span data-ttu-id="68fc4-130">Recupera as propriedades definidas neste objeto com seus valores correspondentes.</span><span class="sxs-lookup"><span data-stu-id="68fc4-130">Retrieves the properties set on this object, with their corresponding values.</span></span><br/>                                                      |
| [<span data-ttu-id="68fc4-131">**LoadFromBlob**</span><span class="sxs-lookup"><span data-stu-id="68fc4-131">**LoadFromBlob**</span></span>](ipropertysetter-loadfromblob.md) | <span data-ttu-id="68fc4-132">Carrega dados de propriedade de um formato de persistência.</span><span class="sxs-lookup"><span data-stu-id="68fc4-132">Loads property data from a persistence format.</span></span><br/>                                                                                     |
| [<span data-ttu-id="68fc4-133">**LoadXML**</span><span class="sxs-lookup"><span data-stu-id="68fc4-133">**LoadXML**</span></span>](ipropertysetter-loadxml.md)           | <span data-ttu-id="68fc4-134">Carrega dados de propriedade expressos em linguagem XML (XML).</span><span class="sxs-lookup"><span data-stu-id="68fc4-134">Loads property data expressed in Extensible Markup Language (XML).</span></span><br/>                                                                 |
| [<span data-ttu-id="68fc4-135">**PrintXML**</span><span class="sxs-lookup"><span data-stu-id="68fc4-135">**PrintXML**</span></span>](ipropertysetter-printxml.md)         | <span data-ttu-id="68fc4-136">Converte dados de propriedade em uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="68fc4-136">Converts property data into an XML string.</span></span><br/>                                                                                         |
| [<span data-ttu-id="68fc4-137">**SaveToBlob**</span><span class="sxs-lookup"><span data-stu-id="68fc4-137">**SaveToBlob**</span></span>](ipropertysetter-savetoblob.md)     | <span data-ttu-id="68fc4-138">Salva os dados de propriedade em um formato de persistência.</span><span class="sxs-lookup"><span data-stu-id="68fc4-138">Saves the property data to a persistence format.</span></span><br/>                                                                                   |
| [<span data-ttu-id="68fc4-139">**Propriedades**</span><span class="sxs-lookup"><span data-stu-id="68fc4-139">**SetProps**</span></span>](ipropertysetter-setprops.md)         | <span data-ttu-id="68fc4-140">Define as propriedades do objeto de destino para o estado apropriado para o tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="68fc4-140">Sets the properties of the target object to the appropriate state for the specified time.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="68fc4-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="68fc4-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68fc4-142">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="68fc4-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="68fc4-143">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="68fc4-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="68fc4-144">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="68fc4-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68fc4-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68fc4-145">Requirements</span></span>



| <span data-ttu-id="68fc4-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="68fc4-146">Requirement</span></span> | <span data-ttu-id="68fc4-147">Valor</span><span class="sxs-lookup"><span data-stu-id="68fc4-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68fc4-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68fc4-148">Header</span></span><br/>  | <dl> <span data-ttu-id="68fc4-149"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="68fc4-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="68fc4-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68fc4-150">Library</span></span><br/> | <dl> <span data-ttu-id="68fc4-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68fc4-151"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
