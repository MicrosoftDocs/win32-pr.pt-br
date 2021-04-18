---
description: Obtém o estado de erro associado à sessão de chave de mídia.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: 'Método IMFMediaKeySession:: GetError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105788799"
---
# <a name="imfmediakeysessiongeterror-method"></a><span data-ttu-id="21344-103">Método IMFMediaKeySession:: GetError</span><span class="sxs-lookup"><span data-stu-id="21344-103">IMFMediaKeySession::GetError method</span></span>

<span data-ttu-id="21344-104">Obtém o estado de erro associado à sessão de chave de mídia.</span><span class="sxs-lookup"><span data-stu-id="21344-104">Gets the error state associated with the media key session.</span></span>

## <a name="syntax"></a><span data-ttu-id="21344-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21344-105">Syntax</span></span>


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a><span data-ttu-id="21344-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21344-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21344-107">*code*</span><span class="sxs-lookup"><span data-stu-id="21344-107">*code*</span></span> 
</dt> <dd>

<span data-ttu-id="21344-108">O código de erro.</span><span class="sxs-lookup"><span data-stu-id="21344-108">The error code.</span></span>

</dd> <dt>

<span data-ttu-id="21344-109">*systemCode*</span><span class="sxs-lookup"><span data-stu-id="21344-109">*systemCode*</span></span> 
</dt> <dd>

<span data-ttu-id="21344-110">Informações de erro específicas da plataforma.</span><span class="sxs-lookup"><span data-stu-id="21344-110">Platform specific error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21344-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21344-111">Return value</span></span>

<span data-ttu-id="21344-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="21344-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21344-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21344-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="21344-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21344-114">Requirements</span></span>



| <span data-ttu-id="21344-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="21344-115">Requirement</span></span> | <span data-ttu-id="21344-116">Valor</span><span class="sxs-lookup"><span data-stu-id="21344-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="21344-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21344-117">Minimum supported client</span></span><br/> | <span data-ttu-id="21344-118">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21344-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="21344-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21344-119">Minimum supported server</span></span><br/> | <span data-ttu-id="21344-120">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="21344-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="21344-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="21344-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21344-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21344-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21344-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="21344-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21344-124">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="21344-124">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




