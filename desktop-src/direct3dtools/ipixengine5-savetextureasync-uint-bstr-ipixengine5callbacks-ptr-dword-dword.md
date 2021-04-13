---
description: Salva uma textura.
MS-HAID: vspixengine.IPixEngine5\_SaveTextureAsync\_UINT\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5:: SaveTextureAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6F08F49E-6FFD-4A9B-86F5-8CB499947F57
api_name:
- IPixEngine5.SaveTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2590f793d0ba05af1ccf9e10ba04fa8b6aa2421b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456853"
---
# <a name="span-idvspixengineipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5savetextureasync-method"></a><span data-ttu-id="b0cd4-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5:: SaveTextureAsync</span><span class="sxs-lookup"><span data-stu-id="b0cd4-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::SaveTextureAsync method</span></span>

<span data-ttu-id="b0cd4-104">Salva uma textura.</span><span class="sxs-lookup"><span data-stu-id="b0cd4-104">Saves a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0cd4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0cd4-105">Syntax</span></span>


```C++
HRESULT SaveTextureAsync(
   UINT                  textureId,
   BSTR                  fileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b0cd4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0cd4-106">Parameters</span></span>

<span data-ttu-id="b0cd4-107">*textureid* </span><span class="sxs-lookup"><span data-stu-id="b0cd4-107">*textureId* </span></span>  
<span data-ttu-id="b0cd4-108">A ID da textura a ser salva.</span><span class="sxs-lookup"><span data-stu-id="b0cd4-108">The ID of the texture to save.</span></span>

<span data-ttu-id="b0cd4-109">*Nome do arquivo* </span><span class="sxs-lookup"><span data-stu-id="b0cd4-109">*fileName* </span></span>  
<span data-ttu-id="b0cd4-110">Uma cadeia de caracteres COM que contém o nome do caminho da textura salva.</span><span class="sxs-lookup"><span data-stu-id="b0cd4-110">A COM string containing the pathname of the saved texture.</span></span>

<span data-ttu-id="b0cd4-111">*retornos* </span><span class="sxs-lookup"><span data-stu-id="b0cd4-111">*callbacks* </span></span>  
<span data-ttu-id="b0cd4-112">O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="b0cd4-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="b0cd4-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b0cd4-113">*requestCookie* </span></span>  
<span data-ttu-id="b0cd4-114">Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="b0cd4-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b0cd4-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b0cd4-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b0cd4-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b0cd4-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0cd4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0cd4-117">Return value</span></span>

<span data-ttu-id="b0cd4-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b0cd4-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0cd4-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0cd4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0cd4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0cd4-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b0cd4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0cd4-121">Header</span></span></p></td><td><span data-ttu-id="b0cd4-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b0cd4-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b0cd4-123"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="b0cd4-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b0cd4-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="b0cd4-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
