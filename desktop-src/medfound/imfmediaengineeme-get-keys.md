---
description: Obtém o objeto de chaves de mídia associado ao mecanismo de mídia ou nulo se não houver um objeto de chaves de mídia.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'Método IMFMediaEngineEME:: get_Keys'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105798233"
---
# <a name="imfmediaengineemeget_keys-method"></a><span data-ttu-id="2e9d8-103">Método IMFMediaEngineEME:: obter \_ chaves</span><span class="sxs-lookup"><span data-stu-id="2e9d8-103">IMFMediaEngineEME::get\_Keys method</span></span>

<span data-ttu-id="2e9d8-104">Obtém o objeto de chaves de mídia associado ao mecanismo de mídia ou **nulo** se não houver um objeto de chaves de mídia.</span><span class="sxs-lookup"><span data-stu-id="2e9d8-104">Gets the media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e9d8-105">Syntax</span></span>


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a><span data-ttu-id="2e9d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e9d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e9d8-107">*novas*</span><span class="sxs-lookup"><span data-stu-id="2e9d8-107">*keys*</span></span> 
</dt> <dd>

<span data-ttu-id="2e9d8-108">O objeto de chaves de mídia associado ao mecanismo de mídia ou **nulo** se não houver um objeto de chaves de mídia.</span><span class="sxs-lookup"><span data-stu-id="2e9d8-108">The media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e9d8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e9d8-109">Return value</span></span>

<span data-ttu-id="2e9d8-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2e9d8-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e9d8-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e9d8-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e9d8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e9d8-112">Requirements</span></span>



| <span data-ttu-id="2e9d8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e9d8-113">Requirement</span></span> | <span data-ttu-id="2e9d8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2e9d8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9d8-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e9d8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9d8-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2e9d8-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2e9d8-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e9d8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9d8-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="2e9d8-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2e9d8-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="2e9d8-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e9d8-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e9d8-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e9d8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e9d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9d8-122">**IMFMediaEngineEME**</span><span class="sxs-lookup"><span data-stu-id="2e9d8-122">**IMFMediaEngineEME**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




