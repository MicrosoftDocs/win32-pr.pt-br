---
description: Atualiza o estado inicial de um objeto; por exemplo, uma textura ou sombreador.
MS-HAID: vspixengine.IPixEngine4\_UpdateObject\_UINT\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine4:: UpdateObject'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90B1DE4F-7DF5-44C9-9A57-1BFB6825EB58
api_name:
- IPixEngine4.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6f21bac93bea44cb7226897a89460788c3900b8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456507"
---
# <a name="span-idvspixengineipixengine4_updateobject_uint_dword_byte_arrspanipixengine4updateobject-method"></a><span data-ttu-id="0c7a8-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>Método IPixEngine4:: UpdateObject</span><span class="sxs-lookup"><span data-stu-id="0c7a8-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4::UpdateObject method</span></span>

<span data-ttu-id="0c7a8-104">Atualiza o estado inicial de um objeto; por exemplo, uma textura ou sombreador.</span><span class="sxs-lookup"><span data-stu-id="0c7a8-104">Updates the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c7a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c7a8-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT    objectAddress,
   DWORD   size,
   BYTE [] count1_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="0c7a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c7a8-106">Parameters</span></span>

<span data-ttu-id="0c7a8-107">*objectaddress* </span><span class="sxs-lookup"><span data-stu-id="0c7a8-107">*objectAddress* </span></span>  
<span data-ttu-id="0c7a8-108">A ID do objeto a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="0c7a8-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="0c7a8-109">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="0c7a8-109">*size* </span></span>  
<span data-ttu-id="0c7a8-110">O tamanho da carga de atualização em bytes.</span><span class="sxs-lookup"><span data-stu-id="0c7a8-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="0c7a8-111">*\_buffer count1* </span><span class="sxs-lookup"><span data-stu-id="0c7a8-111">*count1\_buffer* </span></span>  
<span data-ttu-id="0c7a8-112">A carga de atualização.</span><span class="sxs-lookup"><span data-stu-id="0c7a8-112">The update payload.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c7a8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c7a8-113">Return value</span></span>

<span data-ttu-id="0c7a8-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c7a8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c7a8-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c7a8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c7a8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c7a8-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0c7a8-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c7a8-117">Header</span></span></p></td><td><span data-ttu-id="0c7a8-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0c7a8-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0c7a8-119"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="0c7a8-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0c7a8-120">**IPixEngine4**</span><span class="sxs-lookup"><span data-stu-id="0c7a8-120">**IPixEngine4**</span></span>](/windows/desktop/direct3dtools/ipixengine4)

 

 
