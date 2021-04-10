---
description: Passa recursos para o mecanismo, como cadeias de caracteres para mensagens de erro.
MS-HAID: vspixengine.IPixEngine3\_SetupResources\_ResourcePair\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine3:: SetupResources'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1BB4BE17-51A2-4BA4-81F5-3678B7D5802B
api_name:
- IPixEngine3.SetupResources
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c2b103c5c27bf3929f72d909c9000a1e252e8dee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087675"
---
# <a name="span-idvspixengineipixengine3_setupresources_resourcepair_arr_uintspanipixengine3setupresources-method"></a><span data-ttu-id="66366-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>Método IPixEngine3:: SetupResources</span><span class="sxs-lookup"><span data-stu-id="66366-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3::SetupResources method</span></span>

<span data-ttu-id="66366-104">Passa recursos para o mecanismo, como cadeias de caracteres para mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="66366-104">Passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="66366-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66366-105">Syntax</span></span>


```C++
HRESULT SetupResources(
   ResourcePair [] count1_resources,
   UINT            count
);
```

## <a name="parameters"></a><span data-ttu-id="66366-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66366-106">Parameters</span></span>

<span data-ttu-id="66366-107">*recursos do count1 \_* </span><span class="sxs-lookup"><span data-stu-id="66366-107">*count1\_resources* </span></span>  
<span data-ttu-id="66366-108">Os recursos repassados.</span><span class="sxs-lookup"><span data-stu-id="66366-108">The resources resources passed.</span></span>

<span data-ttu-id="66366-109">*contar* </span><span class="sxs-lookup"><span data-stu-id="66366-109">*count* </span></span>  
<span data-ttu-id="66366-110">O número de recursos passados.</span><span class="sxs-lookup"><span data-stu-id="66366-110">The number of resources passed.</span></span>

## <a name="return-value"></a><span data-ttu-id="66366-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66366-111">Return value</span></span>

<span data-ttu-id="66366-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="66366-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66366-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66366-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="66366-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66366-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="66366-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66366-115">Header</span></span></p></td><td><span data-ttu-id="66366-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="66366-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="66366-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="66366-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="66366-118">**IPixEngine3**</span><span class="sxs-lookup"><span data-stu-id="66366-118">**IPixEngine3**</span></span>](/windows/desktop/direct3dtools/ipixengine3)

 

 
