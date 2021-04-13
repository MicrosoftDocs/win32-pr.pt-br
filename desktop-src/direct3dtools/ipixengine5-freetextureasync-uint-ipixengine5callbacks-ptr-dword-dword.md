---
description: Libera uma textura e notifica o host de forma assíncrona.
MS-HAID: vspixengine.IPixEngine5\_FreeTextureAsync\_UINT\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5:: FreeTextureAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A2D46D4-AA09-4E50-8109-774CE7F538E7
api_name:
- IPixEngine5.FreeTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aed7d29653b9da6f39b1ef6ec4e600c1857744f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456838"
---
# <a name="span-idvspixengineipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dwordspanipixengine5freetextureasync-method"></a><span data-ttu-id="69e0d-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5:: FreeTextureAsync</span><span class="sxs-lookup"><span data-stu-id="69e0d-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::FreeTextureAsync method</span></span>

<span data-ttu-id="69e0d-104">Libera uma textura e notifica o host de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="69e0d-104">Frees a texture and notifies the host asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69e0d-105">Syntax</span></span>


```C++
HRESULT FreeTextureAsync(
   UINT                  textureId,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="69e0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69e0d-106">Parameters</span></span>

<span data-ttu-id="69e0d-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="69e0d-107">*textureId* </span></span>  
<span data-ttu-id="69e0d-108">A ID da textura a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="69e0d-108">The ID of the texture to free..</span></span>

<span data-ttu-id="69e0d-109">*retornos* </span><span class="sxs-lookup"><span data-stu-id="69e0d-109">*callbacks* </span></span>  
<span data-ttu-id="69e0d-110">O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="69e0d-110">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="69e0d-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="69e0d-111">*requestCookie* </span></span>  
<span data-ttu-id="69e0d-112">Um cookie que idenfies exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="69e0d-112">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="69e0d-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="69e0d-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="69e0d-114">Não usado.</span><span class="sxs-lookup"><span data-stu-id="69e0d-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="69e0d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69e0d-115">Return value</span></span>

<span data-ttu-id="69e0d-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="69e0d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69e0d-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69e0d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e0d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69e0d-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="69e0d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69e0d-119">Header</span></span></p></td><td><span data-ttu-id="69e0d-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="69e0d-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="69e0d-121"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="69e0d-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="69e0d-122">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="69e0d-122">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
