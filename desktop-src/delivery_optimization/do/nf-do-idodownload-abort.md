---
title: 'Método IDODownload:: Abort'
description: Anula o download.
keywords:
- 'Método IDODownload:: Abort'
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: babcd5ee00689ac103288074467980777f644668
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105788806"
---
# <a name="idodownloadabort-method"></a><span data-ttu-id="64837-104">Método IDODownload:: Abort</span><span class="sxs-lookup"><span data-stu-id="64837-104">IDODownload::Abort method</span></span>

<span data-ttu-id="64837-105">Anula o download.</span><span class="sxs-lookup"><span data-stu-id="64837-105">Aborts the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="64837-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64837-106">Syntax</span></span>

```cpp
HRESULT Abort();
```

## <a name="return-value"></a><span data-ttu-id="64837-107">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="64837-107">Return Value</span></span>

<span data-ttu-id="64837-108">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="64837-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="64837-109">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="64837-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="64837-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64837-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="64837-111">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="64837-111">**Minimum supported client**</span></span> | <span data-ttu-id="64837-112">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="64837-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="64837-113">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="64837-113">**Minimum supported server**</span></span> | <span data-ttu-id="64837-114">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="64837-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="64837-115">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="64837-115">**Header**</span></span> | <span data-ttu-id="64837-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="64837-116">Do.h</span></span> |
