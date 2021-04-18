---
description: O método SetDynamicReconnectLevel define o nível de reconexão dinâmica durante a renderização.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'Método IRenderEngine:: SetDynamicReconnectLevel (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778465"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a><span data-ttu-id="70279-103">Método IRenderEngine:: SetDynamicReconnectLevel</span><span class="sxs-lookup"><span data-stu-id="70279-103">IRenderEngine::SetDynamicReconnectLevel method</span></span>

> [!Note]  
> <span data-ttu-id="70279-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="70279-104">\[Deprecated.</span></span> <span data-ttu-id="70279-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70279-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="70279-106">O `SetDynamicReconnectLevel` método define o nível de reconexão dinâmica durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="70279-106">The `SetDynamicReconnectLevel` method sets the level of dynamic reconnection during rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="70279-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70279-107">Syntax</span></span>


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="70279-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70279-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70279-109">*Level*</span><span class="sxs-lookup"><span data-stu-id="70279-109">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="70279-110">Combinação de [**sinalizadores de reconexão dinâmica**](dynamic-reconnection-flags.md), especificando o nível de reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="70279-110">Combination of [**Dynamic Reconnection Flags**](dynamic-reconnection-flags.md), specifying the level of dynamic reconnection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70279-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70279-111">Return value</span></span>

<span data-ttu-id="70279-112">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="70279-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="70279-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="70279-113">Return code</span></span>                                                                               | <span data-ttu-id="70279-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="70279-114">Description</span></span>                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="70279-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="70279-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="70279-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="70279-116">Success.</span></span><br/>         |
| <dl> <span data-ttu-id="70279-117"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="70279-117"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="70279-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="70279-118">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="70279-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="70279-119">Remarks</span></span>

<span data-ttu-id="70279-120">Por padrão, o mecanismo de processamento básico carrega cada fonte antes de renderizar um projeto.</span><span class="sxs-lookup"><span data-stu-id="70279-120">By default, the basic render engine loads every source before rendering a project.</span></span> <span data-ttu-id="70279-121">Isso pode resultar em um longo tempo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="70279-121">This can result in a long start-up time.</span></span> <span data-ttu-id="70279-122">Com a reconexão dinâmica, as fontes são carregadas somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="70279-122">With dynamic reconnection, sources are loaded only when needed.</span></span> <span data-ttu-id="70279-123">Isso pode reduzir o tempo de inicialização, mas possivelmente interferir na reprodução suave.</span><span class="sxs-lookup"><span data-stu-id="70279-123">This can shorten the start-up time, but possibly interfere with smooth playback.</span></span> <span data-ttu-id="70279-124">Em geral, quanto mais clipes de origem forem usados por um projeto, mais você poderá se beneficiar da reconexão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="70279-124">Generally, the more source clips that a project uses, the more you might benefit from dynamic reconnection.</span></span>

<span data-ttu-id="70279-125">O mecanismo de processamento inteligente não implementa esse método.</span><span class="sxs-lookup"><span data-stu-id="70279-125">The smart render engine does not implement this method.</span></span>

> [!Note]  
> <span data-ttu-id="70279-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="70279-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="70279-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="70279-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="70279-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="70279-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70279-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70279-129">Requirements</span></span>



| <span data-ttu-id="70279-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="70279-130">Requirement</span></span> | <span data-ttu-id="70279-131">Valor</span><span class="sxs-lookup"><span data-stu-id="70279-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70279-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70279-132">Header</span></span><br/>  | <dl> <span data-ttu-id="70279-133"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="70279-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="70279-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70279-134">Library</span></span><br/> | <dl> <span data-ttu-id="70279-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70279-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70279-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="70279-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70279-137">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="70279-137">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="70279-138">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="70279-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




