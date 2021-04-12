---
title: 'Método IDOManager:: createdownload'
description: Cria um novo download.
keywords:
- 'Método IDOManager:: createdownload'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365343"
---
# <a name="idomanagercreatedownload-method"></a><span data-ttu-id="e1271-104">Método IDOManager:: createdownload</span><span class="sxs-lookup"><span data-stu-id="e1271-104">IDOManager::CreateDownload method</span></span>

<span data-ttu-id="e1271-105">Cria um novo download.</span><span class="sxs-lookup"><span data-stu-id="e1271-105">Creates a new download.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1271-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1271-106">Syntax</span></span>

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a><span data-ttu-id="e1271-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1271-107">Parameters</span></span>

`download`

<span data-ttu-id="e1271-108">O endereço de um ponteiro de interface **IDODownload** .</span><span class="sxs-lookup"><span data-stu-id="e1271-108">The address of an **IDODownload** interface pointer.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1271-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e1271-109">Return Value</span></span>

<span data-ttu-id="e1271-110">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="e1271-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e1271-111">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="e1271-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1271-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1271-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e1271-113">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="e1271-113">**Minimum supported client**</span></span> | <span data-ttu-id="e1271-114">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="e1271-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e1271-115">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="e1271-115">**Minimum supported server**</span></span> | <span data-ttu-id="e1271-116">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="e1271-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e1271-117">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="e1271-117">**Header**</span></span> | <span data-ttu-id="e1271-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="e1271-118">Do.h</span></span> |
