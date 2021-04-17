---
description: Fecha a sessão de chave de mídia e deve ser chamada antes que a sessão de chave seja liberada.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'Método IMFMediaKeySession:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784182"
---
# <a name="imfmediakeysessionclose-method"></a><span data-ttu-id="96e37-103">Método IMFMediaKeySession:: Close</span><span class="sxs-lookup"><span data-stu-id="96e37-103">IMFMediaKeySession::Close method</span></span>

<span data-ttu-id="96e37-104">Fecha a sessão de chave de mídia e deve ser chamada antes que a sessão de chave seja liberada.</span><span class="sxs-lookup"><span data-stu-id="96e37-104">Closes the media key session and must be called before the key session is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e37-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96e37-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="96e37-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96e37-106">Parameters</span></span>

<span data-ttu-id="96e37-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="96e37-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96e37-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96e37-108">Return value</span></span>

<span data-ttu-id="96e37-109">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="96e37-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96e37-110">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96e37-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e37-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96e37-111">Requirements</span></span>



| <span data-ttu-id="96e37-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="96e37-112">Requirement</span></span> | <span data-ttu-id="96e37-113">Valor</span><span class="sxs-lookup"><span data-stu-id="96e37-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96e37-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96e37-114">Minimum supported client</span></span><br/> | <span data-ttu-id="96e37-115">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96e37-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="96e37-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96e37-116">Minimum supported server</span></span><br/> | <span data-ttu-id="96e37-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="96e37-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="96e37-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="96e37-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96e37-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96e37-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e37-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="96e37-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e37-121">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="96e37-121">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




