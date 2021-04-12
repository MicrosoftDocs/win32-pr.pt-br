---
title: 'Método IDODownload:: GetStatus'
description: Recupera um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** que reflete o status atual do download.
keywords:
- 'Método IDODownload:: GetStatus'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365345"
---
# <a name="idodownloadgetstatus-method"></a><span data-ttu-id="51d99-104">Método IDODownload:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="51d99-104">IDODownload::GetStatus method</span></span>

<span data-ttu-id="51d99-105">Recupera um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** que reflete o status atual do download.</span><span class="sxs-lookup"><span data-stu-id="51d99-105">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="51d99-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51d99-106">Syntax</span></span>

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="51d99-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51d99-107">Parameters</span></span>

`status`

<span data-ttu-id="51d99-108">Um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="51d99-108">A pointer to a **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="51d99-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="51d99-109">Return Value</span></span>

<span data-ttu-id="51d99-110">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="51d99-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="51d99-111">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="51d99-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="51d99-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51d99-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="51d99-113">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="51d99-113">**Minimum supported client**</span></span> | <span data-ttu-id="51d99-114">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="51d99-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="51d99-115">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="51d99-115">**Minimum supported server**</span></span> | <span data-ttu-id="51d99-116">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="51d99-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="51d99-117">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="51d99-117">**Header**</span></span> | <span data-ttu-id="51d99-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="51d99-118">Do.h</span></span> |
