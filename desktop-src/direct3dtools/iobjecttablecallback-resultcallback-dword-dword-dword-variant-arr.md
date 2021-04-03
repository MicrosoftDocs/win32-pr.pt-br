---
description: Uma função de retorno de chamada usada para notificar o host das informações da tabela de objetos.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IObjectTableCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646123"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span data-ttu-id="df4e3-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>Método IObjectTableCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="df4e3-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback::ResultCallback method</span></span>

<span data-ttu-id="df4e3-104">Uma função de retorno de chamada usada para notificar o host das informações da tabela de objetos.</span><span class="sxs-lookup"><span data-stu-id="df4e3-104">A callback function used to notify the host of object table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="df4e3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df4e3-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="df4e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df4e3-106">Parameters</span></span>

<span data-ttu-id="df4e3-107">*numElements* </span><span class="sxs-lookup"><span data-stu-id="df4e3-107">*numElements* </span></span>  
<span data-ttu-id="df4e3-108">O número total de campos em todas as colunas de todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="df4e3-108">The total number of fields in all columns of all objects.</span></span>

<span data-ttu-id="df4e3-109">*numRows* </span><span class="sxs-lookup"><span data-stu-id="df4e3-109">*numRows* </span></span>  
<span data-ttu-id="df4e3-110">O número de objetos que estão sendo transferidos.</span><span class="sxs-lookup"><span data-stu-id="df4e3-110">The number of objects being transferred.</span></span>

<span data-ttu-id="df4e3-111">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="df4e3-111">*numColumns* </span></span>  
<span data-ttu-id="df4e3-112">O número de colunas (campos) de informações que estão sendo transferidas para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="df4e3-112">The number of columns (fields) of information being transferred for each object.</span></span>

<span data-ttu-id="df4e3-113">*count0 \_ pRowData* </span><span class="sxs-lookup"><span data-stu-id="df4e3-113">*count0\_pRowData* </span></span>  
<span data-ttu-id="df4e3-114">Informações sobre os objetos; um item para cada campo de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="df4e3-114">Information about the objects; one item for each field of each object.</span></span>

## <a name="return-value"></a><span data-ttu-id="df4e3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df4e3-115">Return value</span></span>

<span data-ttu-id="df4e3-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="df4e3-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="df4e3-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="df4e3-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="df4e3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df4e3-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="df4e3-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df4e3-119">Header</span></span></p></td><td><span data-ttu-id="df4e3-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="df4e3-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="df4e3-121"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="df4e3-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="df4e3-122">**IObjectTableCallback**</span><span class="sxs-lookup"><span data-stu-id="df4e3-122">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
