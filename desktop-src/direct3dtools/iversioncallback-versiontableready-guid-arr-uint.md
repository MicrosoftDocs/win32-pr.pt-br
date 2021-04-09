---
description: Uma função de retorno de chamada usada para notificar o host de quais interfaces têm suporte.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IVersionCallback:: VersionTableReady'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4f31f8b4619d74f6f491f6be8faf7ddd457ee82c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087663"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span data-ttu-id="2f554-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>Método IVersionCallback:: VersionTableReady</span><span class="sxs-lookup"><span data-stu-id="2f554-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback::VersionTableReady method</span></span>

<span data-ttu-id="2f554-104">Uma função de retorno de chamada usada para notificar o host de quais interfaces têm suporte.</span><span class="sxs-lookup"><span data-stu-id="2f554-104">A callback function used to notify the host of which interfaces are supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f554-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f554-105">Syntax</span></span>


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a><span data-ttu-id="2f554-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f554-106">Parameters</span></span>

<span data-ttu-id="2f554-107">*count1 \_ interfaceIds* </span><span class="sxs-lookup"><span data-stu-id="2f554-107">*count1\_interfaceIds* </span></span>  
<span data-ttu-id="2f554-108">Uma matriz que contém os GUIDs de IDs de interface com suporte.</span><span class="sxs-lookup"><span data-stu-id="2f554-108">An array containing the GUIDs of supported interface IDs.</span></span>

<span data-ttu-id="2f554-109">*contar* </span><span class="sxs-lookup"><span data-stu-id="2f554-109">*count* </span></span>  
<span data-ttu-id="2f554-110">O número de GUIDs transmitidos em count1 \_ interfaceIds.</span><span class="sxs-lookup"><span data-stu-id="2f554-110">The number of GUIDs passed in count1\_interfaceIds.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f554-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f554-111">Return value</span></span>

<span data-ttu-id="2f554-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2f554-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f554-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f554-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f554-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f554-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2f554-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f554-115">Header</span></span></p></td><td><span data-ttu-id="2f554-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2f554-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2f554-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="2f554-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2f554-118">**IVersionCallback**</span><span class="sxs-lookup"><span data-stu-id="2f554-118">**IVersionCallback**</span></span>](/windows/desktop/direct3dtools/iversioncallback)

 

 
