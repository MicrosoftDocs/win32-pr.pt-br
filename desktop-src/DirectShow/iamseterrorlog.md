---
description: A interface IAMSetErrorLog define ou recupera um log de erros nos serviços de edição do DirectShow (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interface IAMSetErrorLog (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751228"
---
# <a name="iamseterrorlog-interface"></a><span data-ttu-id="74d8a-103">Interface IAMSetErrorLog</span><span class="sxs-lookup"><span data-stu-id="74d8a-103">IAMSetErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="74d8a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="74d8a-104">\[Deprecated.</span></span> <span data-ttu-id="74d8a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="74d8a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="74d8a-106">A `IAMSetErrorLog` interface define ou recupera um log de erros nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="74d8a-106">The `IAMSetErrorLog` interface sets or retrieves an error log in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="74d8a-107">O objeto Timeline implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="74d8a-107">The timeline object implements this interface.</span></span> <span data-ttu-id="74d8a-108">Os aplicativos podem usar essa interface para registrar erros de renderização em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="74d8a-108">Applications can use this interface to log rendering errors at run time.</span></span> <span data-ttu-id="74d8a-109">Implemente a interface [**IAMErrorLog**](iamerrorlog.md) em seu aplicativo e, em seguida, chame o método [**IAMSetErrorLog::p UT log de \_ erros**](iamseterrorlog-put-errorlog.md) na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="74d8a-109">Implement the [**IAMErrorLog**](iamerrorlog.md) interface in your application, and then call the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span>

<span data-ttu-id="74d8a-110">Para obter mais informações sobre como usar essa interface, consulte [log de erros](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="74d8a-110">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="74d8a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="74d8a-111">Members</span></span>

<span data-ttu-id="74d8a-112">A interface **IAMSetErrorLog** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="74d8a-112">The **IAMSetErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="74d8a-113">**IAMSetErrorLog** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="74d8a-113">**IAMSetErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="74d8a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="74d8a-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="74d8a-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="74d8a-115">Methods</span></span>

<span data-ttu-id="74d8a-116">A interface **IAMSetErrorLog** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="74d8a-116">The **IAMSetErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="74d8a-117">Método</span><span class="sxs-lookup"><span data-stu-id="74d8a-117">Method</span></span>                                               | <span data-ttu-id="74d8a-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="74d8a-118">Description</span></span>                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="74d8a-119">**obter log de \_ erros**</span><span class="sxs-lookup"><span data-stu-id="74d8a-119">**get\_ErrorLog**</span></span>](iamseterrorlog-get-errorlog.md) | <span data-ttu-id="74d8a-120">Recupera o log de erros atual deste objeto.</span><span class="sxs-lookup"><span data-stu-id="74d8a-120">Retrieves the current error log for this object.</span></span><br/> |
| [<span data-ttu-id="74d8a-121">**colocar log de \_ erros**</span><span class="sxs-lookup"><span data-stu-id="74d8a-121">**put\_ErrorLog**</span></span>](iamseterrorlog-put-errorlog.md) | <span data-ttu-id="74d8a-122">Especifica um log de erros para o objeto.</span><span class="sxs-lookup"><span data-stu-id="74d8a-122">Specifies an error log for the object.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="74d8a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="74d8a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="74d8a-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="74d8a-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="74d8a-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="74d8a-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="74d8a-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="74d8a-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="74d8a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74d8a-127">Requirements</span></span>



| <span data-ttu-id="74d8a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="74d8a-128">Requirement</span></span> | <span data-ttu-id="74d8a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="74d8a-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74d8a-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74d8a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="74d8a-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d8a-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="74d8a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74d8a-132">Library</span></span><br/> | <dl> <span data-ttu-id="74d8a-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74d8a-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
