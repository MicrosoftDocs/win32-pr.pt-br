---
description: Função IWICBitmapEncoder_Commit_Proxy function-proxy para o método Commit.
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: Função IWICBitmapEncoder_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 934b2e21097a671c2b52ea77ab07caf25ab521a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091184"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="3a9af-103">Função de proxy de \_ confirmação IWICBitmapEncoder \_</span><span class="sxs-lookup"><span data-stu-id="3a9af-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="3a9af-104">Função de proxy para o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) .</span><span class="sxs-lookup"><span data-stu-id="3a9af-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a9af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a9af-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="3a9af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a9af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a9af-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="3a9af-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a9af-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="3a9af-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="3a9af-109">Ponteiro para este objeto [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="3a9af-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a9af-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3a9af-110">Return value</span></span>

<span data-ttu-id="3a9af-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3a9af-111">Type: **HRESULT**</span></span>

<span data-ttu-id="3a9af-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3a9af-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a9af-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a9af-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a9af-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a9af-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3a9af-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a9af-115">Requirements</span></span>



| <span data-ttu-id="3a9af-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a9af-116">Requirement</span></span> | <span data-ttu-id="3a9af-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3a9af-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a9af-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a9af-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a9af-119">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a9af-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3a9af-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a9af-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a9af-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a9af-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3a9af-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3a9af-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a9af-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a9af-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




