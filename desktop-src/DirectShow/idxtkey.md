---
description: A interface IDxtKey define propriedades na transição de chave. Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição de chave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interface IDxtKey (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779526"
---
# <a name="idxtkey-interface"></a><span data-ttu-id="df7e0-103">Interface IDxtKey</span><span class="sxs-lookup"><span data-stu-id="df7e0-103">IDxtKey interface</span></span>

> [!Note]  
> <span data-ttu-id="df7e0-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="df7e0-104">\[Deprecated.</span></span> <span data-ttu-id="df7e0-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df7e0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="df7e0-106">A `IDxtKey` interface define propriedades na transição de [chave](key-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="df7e0-106">The `IDxtKey` interface sets properties on the [Key](key-transition.md) transition.</span></span>

<span data-ttu-id="df7e0-107">Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição de chave.</span><span class="sxs-lookup"><span data-stu-id="df7e0-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Key transition.</span></span> <span data-ttu-id="df7e0-108">Os aplicativos DES não precisam usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="df7e0-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="df7e0-109">Para definir as propriedades em uma transição em DES, use a interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="df7e0-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="df7e0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="df7e0-110">Members</span></span>

<span data-ttu-id="df7e0-111">A interface **IDxtKey** herda de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="df7e0-111">The **IDxtKey** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="df7e0-112">**IDxtKey** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="df7e0-112">**IDxtKey** also has these types of members:</span></span>

-   [<span data-ttu-id="df7e0-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="df7e0-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="df7e0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="df7e0-114">Methods</span></span>

<span data-ttu-id="df7e0-115">A interface **IDxtKey** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="df7e0-115">The **IDxtKey** interface has these methods.</span></span>



| <span data-ttu-id="df7e0-116">Método</span><span class="sxs-lookup"><span data-stu-id="df7e0-116">Method</span></span>                                            | <span data-ttu-id="df7e0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="df7e0-117">Description</span></span>                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="df7e0-118">**obter \_ matiz**</span><span class="sxs-lookup"><span data-stu-id="df7e0-118">**get\_Hue**</span></span>](idxtkey-get-hue.md)               | <span data-ttu-id="df7e0-119">Recupera o valor de matiz para o qual fazer a chave.</span><span class="sxs-lookup"><span data-stu-id="df7e0-119">Retrieves the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="df7e0-120">**obter \_ inverter**</span><span class="sxs-lookup"><span data-stu-id="df7e0-120">**get\_Invert**</span></span>](idxtkey-get-invert.md)         | <span data-ttu-id="df7e0-121">Recupera um valor booliano que indica se a operação de chave está invertida.</span><span class="sxs-lookup"><span data-stu-id="df7e0-121">Retrieves a Boolean value indicating whether the key operation is inverted.</span></span><br/> |
| [<span data-ttu-id="df7e0-122">**obter \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="df7e0-122">**get\_KeyType**</span></span>](idxtkey-get-keytype.md)       | <span data-ttu-id="df7e0-123">Recupera o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="df7e0-123">Retrieves the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="df7e0-124">**obter \_ luminância**</span><span class="sxs-lookup"><span data-stu-id="df7e0-124">**get\_Luminance**</span></span>](idxtkey-get-luminance.md)   | <span data-ttu-id="df7e0-125">Recupera o valor de luminância no qual a chave deve ser Key.</span><span class="sxs-lookup"><span data-stu-id="df7e0-125">Retrieves the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="df7e0-126">**obter \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="df7e0-126">**get\_RGB**</span></span>](idxtkey-get-rgb.md)               | <span data-ttu-id="df7e0-127">Recupera a cor RGB para a chave.</span><span class="sxs-lookup"><span data-stu-id="df7e0-127">Retrieves the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="df7e0-128">**obter \_ similaridade**</span><span class="sxs-lookup"><span data-stu-id="df7e0-128">**get\_Similarity**</span></span>](idxtkey-get-similarity.md) | <span data-ttu-id="df7e0-129">Recupera o intervalo de dados de cor que se torna transparente.</span><span class="sxs-lookup"><span data-stu-id="df7e0-129">Retrieves the range of color data that becomes transparent.</span></span><br/>                 |
| [<span data-ttu-id="df7e0-130">**colocar \_ matiz**</span><span class="sxs-lookup"><span data-stu-id="df7e0-130">**put\_Hue**</span></span>](idxtkey-put-hue.md)               | <span data-ttu-id="df7e0-131">Especifica o valor de matiz a ser chaveada.</span><span class="sxs-lookup"><span data-stu-id="df7e0-131">Specifies the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="df7e0-132">**colocar \_ inverter**</span><span class="sxs-lookup"><span data-stu-id="df7e0-132">**put\_Invert**</span></span>](idxtkey-put-invert.md)         | <span data-ttu-id="df7e0-133">Especifica se a operação de chave está invertida.</span><span class="sxs-lookup"><span data-stu-id="df7e0-133">Specifies whether the key operation is inverted.</span></span><br/>                            |
| [<span data-ttu-id="df7e0-134">**colocar \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="df7e0-134">**put\_KeyType**</span></span>](idxtkey-put-keytype.md)       | <span data-ttu-id="df7e0-135">Especifica o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="df7e0-135">Specifies the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="df7e0-136">**colocar \_ luminância**</span><span class="sxs-lookup"><span data-stu-id="df7e0-136">**put\_Luminance**</span></span>](idxtkey-put-luminance.md)   | <span data-ttu-id="df7e0-137">Especifica o valor de luminância para a chave.</span><span class="sxs-lookup"><span data-stu-id="df7e0-137">Specifies the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="df7e0-138">**colocar \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="df7e0-138">**put\_RGB**</span></span>](idxtkey-put-rgb.md)               | <span data-ttu-id="df7e0-139">Especifica a cor RGB para a chave.</span><span class="sxs-lookup"><span data-stu-id="df7e0-139">Specifies the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="df7e0-140">**colocar \_ similaridade**</span><span class="sxs-lookup"><span data-stu-id="df7e0-140">**put\_Similarity**</span></span>](idxtkey-put-similarity.md) | <span data-ttu-id="df7e0-141">Especifica o intervalo de dados de cor que se torna transparente.</span><span class="sxs-lookup"><span data-stu-id="df7e0-141">Specifies the range of color data that becomes transparent.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="df7e0-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="df7e0-142">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="df7e0-143">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="df7e0-143">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="df7e0-144">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="df7e0-144">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="df7e0-145">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="df7e0-145">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df7e0-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df7e0-146">Requirements</span></span>



| <span data-ttu-id="df7e0-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="df7e0-147">Requirement</span></span> | <span data-ttu-id="df7e0-148">Valor</span><span class="sxs-lookup"><span data-stu-id="df7e0-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df7e0-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df7e0-149">Header</span></span><br/>  | <dl> <span data-ttu-id="df7e0-150"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="df7e0-150"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="df7e0-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df7e0-151">Library</span></span><br/> | <dl> <span data-ttu-id="df7e0-152"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df7e0-152"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




