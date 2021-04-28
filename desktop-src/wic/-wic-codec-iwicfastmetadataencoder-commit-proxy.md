---
description: Função IWICFastMetadataEncoder_Commit_Proxy function-proxy para o método Commit.
ms.assetid: 5b3b90ad-9d67-4fbd-b01e-c7478df8dd45
title: Função IWICFastMetadataEncoder_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 848ed74ec9c9bb490065935bd94cae7a35d02db2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097184"
---
# <a name="iwicfastmetadataencoder_commit_proxy-function"></a><span data-ttu-id="19a0f-103">Função de proxy de \_ confirmação IWICFastMetadataEncoder \_</span><span class="sxs-lookup"><span data-stu-id="19a0f-103">IWICFastMetadataEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="19a0f-104">Função de proxy para o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) .</span><span class="sxs-lookup"><span data-stu-id="19a0f-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="19a0f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19a0f-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_Commit_Proxy(
  _In_ IWICFastMetadataEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="19a0f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19a0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a0f-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="19a0f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19a0f-108">Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***</span><span class="sxs-lookup"><span data-stu-id="19a0f-108">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\***</span></span>

<span data-ttu-id="19a0f-109">Ponteiro para este objeto [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="19a0f-109">Pointer to this [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a0f-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="19a0f-110">Return value</span></span>

<span data-ttu-id="19a0f-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="19a0f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="19a0f-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="19a0f-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19a0f-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19a0f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19a0f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="19a0f-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="19a0f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19a0f-115">Requirements</span></span>



| <span data-ttu-id="19a0f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="19a0f-116">Requirement</span></span> | <span data-ttu-id="19a0f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="19a0f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a0f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19a0f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="19a0f-119">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19a0f-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="19a0f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19a0f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="19a0f-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19a0f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="19a0f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="19a0f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19a0f-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19a0f-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




