---
title: 'Método IDODownload:: Finalize'
description: Finaliza o download.
keywords:
- 'Método IDODownload:: Finalize'
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105762222"
---
# <a name="idodownloadfinalize-method"></a><span data-ttu-id="82a5e-104">Método IDODownload:: Finalize</span><span class="sxs-lookup"><span data-stu-id="82a5e-104">IDODownload::Finalize method</span></span>

<span data-ttu-id="82a5e-105">Finaliza o download.</span><span class="sxs-lookup"><span data-stu-id="82a5e-105">Finalizes the download.</span></span> <span data-ttu-id="82a5e-106">Depois de finalizado, um download não pode ser retomado chamando **Start**.</span><span class="sxs-lookup"><span data-stu-id="82a5e-106">Once finalized, a download cannot be resumed by calling **Start**.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a5e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82a5e-107">Syntax</span></span>

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a><span data-ttu-id="82a5e-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="82a5e-108">Return Value</span></span>

<span data-ttu-id="82a5e-109">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="82a5e-109">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="82a5e-110">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="82a5e-110">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="82a5e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82a5e-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="82a5e-112">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="82a5e-112">**Minimum supported client**</span></span> | <span data-ttu-id="82a5e-113">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="82a5e-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="82a5e-114">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="82a5e-114">**Minimum supported server**</span></span> | <span data-ttu-id="82a5e-115">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="82a5e-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="82a5e-116">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="82a5e-116">**Header**</span></span> | <span data-ttu-id="82a5e-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="82a5e-117">Do.h</span></span> |
