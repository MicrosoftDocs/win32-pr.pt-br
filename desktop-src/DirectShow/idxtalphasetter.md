---
description: A interface IDxtAlphaSetter define propriedades no efeito de setter alfa. Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza o efeito de setter alfa.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interface IDxtAlphaSetter (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759292"
---
# <a name="idxtalphasetter-interface"></a><span data-ttu-id="11d7f-103">Interface IDxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="11d7f-103">IDxtAlphaSetter interface</span></span>

> [!Note]  
> <span data-ttu-id="11d7f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="11d7f-104">\[Deprecated.</span></span> <span data-ttu-id="11d7f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="11d7f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="11d7f-106">A `IDxtAlphaSetter` interface define propriedades no efeito de [setter alfa](alpha-setter-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="11d7f-106">The `IDxtAlphaSetter` interface sets properties on the [Alpha Setter](alpha-setter-effect.md) effect.</span></span>

<span data-ttu-id="11d7f-107">Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza o efeito de setter alfa.</span><span class="sxs-lookup"><span data-stu-id="11d7f-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Alpha Setter effect.</span></span> <span data-ttu-id="11d7f-108">Os aplicativos DES não precisam usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="11d7f-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="11d7f-109">Para definir as propriedades em uma transição em DES, use a interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="11d7f-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="11d7f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="11d7f-110">Members</span></span>

<span data-ttu-id="11d7f-111">A interface **IDxtAlphaSetter** herda de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="11d7f-111">The **IDxtAlphaSetter** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="11d7f-112">**IDxtAlphaSetter** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="11d7f-112">**IDxtAlphaSetter** also has these types of members:</span></span>

-   [<span data-ttu-id="11d7f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="11d7f-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11d7f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="11d7f-114">Methods</span></span>

<span data-ttu-id="11d7f-115">A interface **IDxtAlphaSetter** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="11d7f-115">The **IDxtAlphaSetter** interface has these methods.</span></span>



| <span data-ttu-id="11d7f-116">Método</span><span class="sxs-lookup"><span data-stu-id="11d7f-116">Method</span></span>                                                  | <span data-ttu-id="11d7f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="11d7f-117">Description</span></span>                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="11d7f-118">**obter \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="11d7f-118">**get\_Alpha**</span></span>](idxtalphasetter-get-alpha.md)         | <span data-ttu-id="11d7f-119">Recupera o valor alfa de toda a imagem.</span><span class="sxs-lookup"><span data-stu-id="11d7f-119">Retrieves the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="11d7f-120">**obter \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="11d7f-120">**get\_AlphaRamp**</span></span>](idxtalphasetter-get-alpharamp.md) | <span data-ttu-id="11d7f-121">Recupera a propriedade de rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="11d7f-121">Retrieves the alpha ramp property.</span></span><br/>              |
| [<span data-ttu-id="11d7f-122">**colocar \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="11d7f-122">**put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)         | <span data-ttu-id="11d7f-123">Especifica o valor alfa para a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="11d7f-123">Specifies the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="11d7f-124">**colocar \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="11d7f-124">**put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md) | <span data-ttu-id="11d7f-125">Especifica a propriedade de rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="11d7f-125">Specifies the alpha ramp property.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="11d7f-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="11d7f-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="11d7f-127">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="11d7f-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="11d7f-128">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="11d7f-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="11d7f-129">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="11d7f-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11d7f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11d7f-130">Requirements</span></span>



| <span data-ttu-id="11d7f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d7f-131">Requirement</span></span> | <span data-ttu-id="11d7f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="11d7f-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11d7f-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11d7f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="11d7f-134"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d7f-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="11d7f-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11d7f-135">Library</span></span><br/> | <dl> <span data-ttu-id="11d7f-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11d7f-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




