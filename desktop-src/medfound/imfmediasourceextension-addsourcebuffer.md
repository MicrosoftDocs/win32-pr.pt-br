---
description: Adiciona um IMFSourceBuffer à coleção de buffers associados ao IMFMediaSourceExtension.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: 'Método IMFMediaSourceExtension:: AddSourceBuffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105790573"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a><span data-ttu-id="0f83c-103">Método IMFMediaSourceExtension:: AddSourceBuffer</span><span class="sxs-lookup"><span data-stu-id="0f83c-103">IMFMediaSourceExtension::AddSourceBuffer method</span></span>

<span data-ttu-id="0f83c-104">Adiciona um [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) à coleção de buffers associados ao [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span><span class="sxs-lookup"><span data-stu-id="0f83c-104">Adds a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) to the collection of buffers associated with the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f83c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f83c-105">Syntax</span></span>


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0f83c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f83c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f83c-107">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="0f83c-107">*type* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0f83c-108">*pNotify* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f83c-108">*pNotify* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0f83c-109">*ppSourceBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f83c-109">*ppSourceBuffer* \[out\]</span></span>
<span data-ttu-id="0f83c-110"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0f83c-110"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="0f83c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f83c-111">Return value</span></span>

<span data-ttu-id="0f83c-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f83c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f83c-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f83c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f83c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f83c-114">Requirements</span></span>



| <span data-ttu-id="0f83c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f83c-115">Requirement</span></span> | <span data-ttu-id="0f83c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0f83c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f83c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f83c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f83c-118">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0f83c-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0f83c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f83c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f83c-120">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="0f83c-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0f83c-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="0f83c-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f83c-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f83c-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f83c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f83c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f83c-124">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="0f83c-124">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




