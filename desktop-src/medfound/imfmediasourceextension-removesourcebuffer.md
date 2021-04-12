---
description: Remove o buffer de origem especificado da coleção de buffers de origem gerenciados pelo objeto IMFMediaSourceExtension.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'Método IMFMediaSourceExtension:: RemoveSourceBuffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297952"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a><span data-ttu-id="9e367-103">Método IMFMediaSourceExtension:: RemoveSourceBuffer</span><span class="sxs-lookup"><span data-stu-id="9e367-103">IMFMediaSourceExtension::RemoveSourceBuffer method</span></span>

<span data-ttu-id="9e367-104">Remove o buffer de origem especificado da coleção de buffers de origem gerenciados pelo objeto [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) .</span><span class="sxs-lookup"><span data-stu-id="9e367-104">Removes the specified source buffer from the collection of source buffers managed by the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e367-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e367-105">Syntax</span></span>


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="9e367-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e367-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e367-107">*pSourceBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e367-107">*pSourceBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e367-108">O buffer a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9e367-108">The buffer to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e367-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e367-109">Return value</span></span>

<span data-ttu-id="9e367-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9e367-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e367-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e367-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e367-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e367-112">Requirements</span></span>



| <span data-ttu-id="9e367-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e367-113">Requirement</span></span> | <span data-ttu-id="9e367-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9e367-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e367-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e367-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9e367-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e367-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9e367-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e367-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9e367-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="9e367-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9e367-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="9e367-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e367-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e367-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e367-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e367-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e367-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="9e367-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




