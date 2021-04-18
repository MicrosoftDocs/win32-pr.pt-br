---
description: Obtém uma ID de sessão exclusiva criada para esta sessão.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: 'Método IMFMediaKeySession:: get_SessionId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105778788"
---
# <a name="imfmediakeysessionget_sessionid-method"></a><span data-ttu-id="e1880-103">Método IMFMediaKeySession:: get \_ SessionID</span><span class="sxs-lookup"><span data-stu-id="e1880-103">IMFMediaKeySession::get\_SessionId method</span></span>

<span data-ttu-id="e1880-104">Obtém uma ID de sessão exclusiva criada para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="e1880-104">Gets a unique session id created for this session.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1880-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1880-105">Syntax</span></span>


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a><span data-ttu-id="e1880-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1880-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1880-107">*sessionId*</span><span class="sxs-lookup"><span data-stu-id="e1880-107">*sessionId*</span></span> 
</dt> <dd>

<span data-ttu-id="e1880-108">A ID da sessão da chave de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1880-108">The media key session id.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1880-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1880-109">Return value</span></span>

<span data-ttu-id="e1880-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e1880-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e1880-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e1880-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1880-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1880-112">Requirements</span></span>



| <span data-ttu-id="e1880-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1880-113">Requirement</span></span> | <span data-ttu-id="e1880-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e1880-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1880-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1880-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e1880-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1880-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e1880-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1880-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e1880-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="e1880-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e1880-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="e1880-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1880-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1880-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1880-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1880-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1880-122">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="e1880-122">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




