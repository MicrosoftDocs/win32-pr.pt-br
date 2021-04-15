---
description: Uma solicitação para atualizar o estado inicial de um objeto; por exemplo, uma textura ou sombreador.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IUpdateObject:: UpdateObject'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b04918878de15a2b9a5b004d3dff252ab3ddc9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456694"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span data-ttu-id="3acff-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>Método IUpdateObject:: UpdateObject</span><span class="sxs-lookup"><span data-stu-id="3acff-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject method</span></span>

<span data-ttu-id="3acff-104">Uma solicitação para atualizar o estado inicial de um objeto; por exemplo, uma textura ou sombreador.</span><span class="sxs-lookup"><span data-stu-id="3acff-104">A request to update the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="3acff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3acff-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="3acff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3acff-106">Parameters</span></span>

<span data-ttu-id="3acff-107">*objectaddress* </span><span class="sxs-lookup"><span data-stu-id="3acff-107">*objectAddress* </span></span>  
<span data-ttu-id="3acff-108">A ID do objeto a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="3acff-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="3acff-109">*tamanho* </span><span class="sxs-lookup"><span data-stu-id="3acff-109">*size* </span></span>  
<span data-ttu-id="3acff-110">O tamanho da carga de atualização em bytes.</span><span class="sxs-lookup"><span data-stu-id="3acff-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="3acff-111">*\_buffer count1* </span><span class="sxs-lookup"><span data-stu-id="3acff-111">*count1\_buffer* </span></span>  
<span data-ttu-id="3acff-112">A carga de atualização.</span><span class="sxs-lookup"><span data-stu-id="3acff-112">The update payload.</span></span>

<span data-ttu-id="3acff-113">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="3acff-113">*pCallback* </span></span>  
<span data-ttu-id="3acff-114">O endereço de uma função usada para notificar o host de que o objeto foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="3acff-114">The address of a function used to notify the host that the object was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="3acff-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3acff-115">Return value</span></span>

<span data-ttu-id="3acff-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3acff-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3acff-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3acff-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3acff-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3acff-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3acff-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3acff-119">Header</span></span></p></td><td><span data-ttu-id="3acff-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3acff-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3acff-121"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="3acff-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3acff-122">**IUpdateObject**</span><span class="sxs-lookup"><span data-stu-id="3acff-122">**IUpdateObject**</span></span>](/windows/desktop/direct3dtools/iupdateobject)

 

 
