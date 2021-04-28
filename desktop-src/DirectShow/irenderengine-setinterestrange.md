---
description: 'Método IRenderEngine:: SetInterestRange-sem suporte.'
ms.assetid: 1e4c3bd4-2540-428f-9ca6-dd4c65c53434
title: 'Método IRenderEngine:: SetInterestRange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetInterestRange
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec9790e65efa30b83cf324da4153f20c541733b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084454"
---
# <a name="irenderenginesetinterestrange-method"></a><span data-ttu-id="31455-103">Método IRenderEngine:: SetInterestRange</span><span class="sxs-lookup"><span data-stu-id="31455-103">IRenderEngine::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="31455-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="31455-104">\[Deprecated.</span></span> <span data-ttu-id="31455-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="31455-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="31455-106">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="31455-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="31455-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31455-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="31455-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31455-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31455-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="31455-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="31455-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="31455-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="31455-111">*Parar*</span><span class="sxs-lookup"><span data-stu-id="31455-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="31455-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="31455-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31455-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="31455-113">Return value</span></span>

<span data-ttu-id="31455-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="31455-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31455-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31455-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="31455-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="31455-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="31455-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="31455-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="31455-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="31455-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="31455-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="31455-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="31455-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="31455-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31455-121">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="31455-121">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> </dl>

 

 



