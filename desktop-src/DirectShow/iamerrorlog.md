---
description: A interface IAMErrorLog fornece um método de retorno de chamada para log de erros nos serviços de edição do DirectShow (DES). O DES não implementa essa interface.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interface IAMErrorLog (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757297"
---
# <a name="iamerrorlog-interface"></a><span data-ttu-id="beb9d-103">Interface IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="beb9d-103">IAMErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="beb9d-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="beb9d-104">\[Deprecated.</span></span> <span data-ttu-id="beb9d-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="beb9d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="beb9d-106">A `IAMErrorLog` interface fornece um método de retorno de chamada para log de erros nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="beb9d-106">The `IAMErrorLog` interface provides a callback method for error logging in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="beb9d-107">O DES não implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="beb9d-107">DES does not implement this interface.</span></span> <span data-ttu-id="beb9d-108">Para executar o log de erros, implemente essa interface em seu aplicativo e chame [**IAMSetErrorLog \_ ::p UT**](iamseterrorlog-put-errorlog.md) log de erros na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="beb9d-108">To perform error logging, implement this interface in your application and call [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) on the timeline.</span></span> <span data-ttu-id="beb9d-109">Se ocorrer um erro quando você renderizar o projeto, o DES chamará o método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) implementado pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="beb9d-109">If an error occurs when you render the project, DES will call the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method implemented by your application.</span></span>

<span data-ttu-id="beb9d-110">O DES registra erros somente quando você renderiza um projeto usando a interface [**IRenderEngine**](irenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="beb9d-110">DES logs errors only when you render a project using the [**IRenderEngine**](irenderengine.md) interface.</span></span> <span data-ttu-id="beb9d-111">Por exemplo, se você salvar um projeto como um grafo de filtro do DirectShow (formato. GRF) e reproduzir o arquivo de grafo, não haverá log de erros.</span><span class="sxs-lookup"><span data-stu-id="beb9d-111">For example, if you save a project as a DirectShow filter graph (.grf format) and play the graph file, there is no error logging.</span></span> <span data-ttu-id="beb9d-112">Para obter mais informações sobre como usar essa interface, consulte [log de erros](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="beb9d-112">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="beb9d-113">Membros</span><span class="sxs-lookup"><span data-stu-id="beb9d-113">Members</span></span>

<span data-ttu-id="beb9d-114">A interface **IAMErrorLog** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="beb9d-114">The **IAMErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="beb9d-115">**IAMErrorLog** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="beb9d-115">**IAMErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="beb9d-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="beb9d-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="beb9d-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="beb9d-117">Methods</span></span>

<span data-ttu-id="beb9d-118">A interface **IAMErrorLog** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="beb9d-118">The **IAMErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="beb9d-119">Método</span><span class="sxs-lookup"><span data-stu-id="beb9d-119">Method</span></span>                                   | <span data-ttu-id="beb9d-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="beb9d-120">Description</span></span>               |
|:-----------------------------------------|:--------------------------|
| [<span data-ttu-id="beb9d-121">**LogError**</span><span class="sxs-lookup"><span data-stu-id="beb9d-121">**LogError**</span></span>](iamerrorlog-logerror.md) | <span data-ttu-id="beb9d-122">Registra um erro.</span><span class="sxs-lookup"><span data-stu-id="beb9d-122">Logs an error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="beb9d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="beb9d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="beb9d-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="beb9d-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="beb9d-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="beb9d-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="beb9d-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="beb9d-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="beb9d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beb9d-127">Requirements</span></span>



| <span data-ttu-id="beb9d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb9d-128">Requirement</span></span> | <span data-ttu-id="beb9d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="beb9d-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beb9d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="beb9d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="beb9d-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb9d-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="beb9d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="beb9d-132">Library</span></span><br/> | <dl> <span data-ttu-id="beb9d-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beb9d-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
