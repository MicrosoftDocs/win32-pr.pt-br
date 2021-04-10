---
description: Acrescenta o segmento de mídia especificado ao IMFSourceBuffer.
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: 'Método IMFSourceBuffer:: Append'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 00c9b6a0af2e48482311a8a0e1bc39dc4ce951aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164767"
---
# <a name="imfsourcebufferappend-method"></a><span data-ttu-id="3cd27-103">Método IMFSourceBuffer:: Append</span><span class="sxs-lookup"><span data-stu-id="3cd27-103">IMFSourceBuffer::Append method</span></span>

<span data-ttu-id="3cd27-104">Acrescenta o segmento de mídia especificado ao [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="3cd27-104">Appends the specified media segment to the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd27-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cd27-105">Syntax</span></span>


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a><span data-ttu-id="3cd27-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cd27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cd27-107">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3cd27-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cd27-108">Os dados de mídia a serem acrescentados.</span><span class="sxs-lookup"><span data-stu-id="3cd27-108">The media data to append.</span></span>

</dd> <dt>

<span data-ttu-id="3cd27-109">*Len* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3cd27-109">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cd27-110">O comprimento dos dados de mídia armazenados em *pData*.</span><span class="sxs-lookup"><span data-stu-id="3cd27-110">The length of the media data stored in *pData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cd27-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cd27-111">Return value</span></span>

<span data-ttu-id="3cd27-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3cd27-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3cd27-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3cd27-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd27-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cd27-114">Requirements</span></span>



| <span data-ttu-id="3cd27-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cd27-115">Requirement</span></span> | <span data-ttu-id="3cd27-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3cd27-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd27-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cd27-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3cd27-118">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3cd27-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3cd27-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cd27-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3cd27-120">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="3cd27-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3cd27-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="3cd27-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3cd27-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3cd27-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cd27-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cd27-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cd27-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="3cd27-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




