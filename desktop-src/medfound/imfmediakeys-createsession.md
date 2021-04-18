---
description: Cria um objeto de sessão de chave de mídia usando os dados de inicialização especificados e os dados personalizados. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'Método IMFMediaKeys:: CreateSession'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105813481"
---
# <a name="imfmediakeyscreatesession-method"></a><span data-ttu-id="32439-104">Método IMFMediaKeys:: CreateSession</span><span class="sxs-lookup"><span data-stu-id="32439-104">IMFMediaKeys::CreateSession method</span></span>

<span data-ttu-id="32439-105">Cria um objeto de sessão de chave de mídia usando os dados de inicialização especificados e os dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="32439-105">Creates a media key session object using the specified initialization data and custom data.</span></span> <span data-ttu-id="32439-106">.</span><span class="sxs-lookup"><span data-stu-id="32439-106">.</span></span>

## <a name="syntax"></a><span data-ttu-id="32439-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32439-107">Syntax</span></span>


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a><span data-ttu-id="32439-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32439-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32439-109">*MIME*</span><span class="sxs-lookup"><span data-stu-id="32439-109">*mimeType*</span></span> 
</dt> <dd>

<span data-ttu-id="32439-110">O tipo MIME do contêiner de mídia usado para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="32439-110">The MIME type of the media container used for the content.</span></span>

</dd> <dt>

<span data-ttu-id="32439-111">*initData*</span><span class="sxs-lookup"><span data-stu-id="32439-111">*initData*</span></span> 
</dt> <dd>

<span data-ttu-id="32439-112">Os dados de inicialização para o sistema de chaves.</span><span class="sxs-lookup"><span data-stu-id="32439-112">The initialization data for the key system.</span></span>

</dd> <dt>

<span data-ttu-id="32439-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="32439-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="32439-114">A contagem em bytes de *initdata*.</span><span class="sxs-lookup"><span data-stu-id="32439-114">The count in bytes of *initData*.</span></span>

</dd> <dt>

<span data-ttu-id="32439-115">*customData*</span><span class="sxs-lookup"><span data-stu-id="32439-115">*customData*</span></span> 
</dt> <dd>

<span data-ttu-id="32439-116">Dados personalizados enviados para o sistema de chaves.</span><span class="sxs-lookup"><span data-stu-id="32439-116">Custom data sent to the key system.</span></span>

</dd> <dt>

<span data-ttu-id="32439-117">*cbCustomData*</span><span class="sxs-lookup"><span data-stu-id="32439-117">*cbCustomData*</span></span> 
</dt> <dd>

<span data-ttu-id="32439-118">A contagem em bytes de *cbCustomData*.</span><span class="sxs-lookup"><span data-stu-id="32439-118">The count in bytes of *cbCustomData*.</span></span>

</dd> <dt>

<span data-ttu-id="32439-119">*sobre*</span><span class="sxs-lookup"><span data-stu-id="32439-119">*notify*</span></span> 
</dt> <dd>

<span data-ttu-id="32439-120">sobre</span><span class="sxs-lookup"><span data-stu-id="32439-120">notify</span></span>

</dd> <dt>

<span data-ttu-id="32439-121">*ppSession*</span><span class="sxs-lookup"><span data-stu-id="32439-121">*ppSession*</span></span> 
</dt> <dd>

<span data-ttu-id="32439-122">A sessão de chave de mídia.</span><span class="sxs-lookup"><span data-stu-id="32439-122">The media key session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32439-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32439-123">Return value</span></span>

<span data-ttu-id="32439-124">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="32439-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32439-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32439-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="32439-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32439-126">Requirements</span></span>



| <span data-ttu-id="32439-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="32439-127">Requirement</span></span> | <span data-ttu-id="32439-128">Valor</span><span class="sxs-lookup"><span data-stu-id="32439-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="32439-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32439-129">Minimum supported client</span></span><br/> | <span data-ttu-id="32439-130">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="32439-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="32439-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32439-131">Minimum supported server</span></span><br/> | <span data-ttu-id="32439-132">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="32439-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="32439-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="32439-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32439-134"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32439-134"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32439-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="32439-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32439-136">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="32439-136">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




