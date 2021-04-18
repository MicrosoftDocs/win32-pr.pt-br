---
description: O método ScrapIt descarta o grafo de filtro do mecanismo de processamento e todos os objetos associados.
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: 'Método IRenderEngine:: ScrapIt (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f9febbe20cfd5ab9a6577a6e00989c7d6fc4145
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778432"
---
# <a name="irenderenginescrapit-method"></a><span data-ttu-id="4465d-103">Método IRenderEngine:: ScrapIt</span><span class="sxs-lookup"><span data-stu-id="4465d-103">IRenderEngine::ScrapIt method</span></span>

> [!Note]  
> <span data-ttu-id="4465d-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4465d-104">\[Deprecated.</span></span> <span data-ttu-id="4465d-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4465d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4465d-106">O `ScrapIt` método descarta o grafo de filtro do mecanismo de renderização e todos os objetos associados.</span><span class="sxs-lookup"><span data-stu-id="4465d-106">The `ScrapIt` method discards the render engine's filter graph and all associated objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="4465d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4465d-107">Syntax</span></span>


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a><span data-ttu-id="4465d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4465d-108">Parameters</span></span>

<span data-ttu-id="4465d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4465d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4465d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4465d-110">Return value</span></span>

<span data-ttu-id="4465d-111">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="4465d-111">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="4465d-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4465d-112">Return code</span></span>                                                                                            | <span data-ttu-id="4465d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4465d-113">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4465d-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4465d-114"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="4465d-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="4465d-115">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="4465d-116"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="4465d-116"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="4465d-117">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="4465d-117">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4465d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4465d-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4465d-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="4465d-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4465d-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4465d-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4465d-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4465d-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4465d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4465d-122">Requirements</span></span>



| <span data-ttu-id="4465d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4465d-123">Requirement</span></span> | <span data-ttu-id="4465d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4465d-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4465d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4465d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4465d-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4465d-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4465d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4465d-127">Library</span></span><br/> | <dl> <span data-ttu-id="4465d-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4465d-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4465d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4465d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4465d-130">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="4465d-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="4465d-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="4465d-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




