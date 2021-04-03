---
title: 'IDODownload: método ause de:P'
description: Pausa o download.
keywords:
- 'IDODownload: método ause de:P'
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7239253238b0d9b7e606329b10f05b3645b7e16
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104084289"
---
# <a name="idodownloadpause-method"></a><span data-ttu-id="feffa-104">IDODownload: método ause de:P</span><span class="sxs-lookup"><span data-stu-id="feffa-104">IDODownload::Pause method</span></span>

<span data-ttu-id="feffa-105">Pausa o download.</span><span class="sxs-lookup"><span data-stu-id="feffa-105">Pauses the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="feffa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="feffa-106">Syntax</span></span>

```cpp
HRESULT Pause();
```

## <a name="return-value"></a><span data-ttu-id="feffa-107">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="feffa-107">Return Value</span></span>

<span data-ttu-id="feffa-108">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="feffa-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="feffa-109">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="feffa-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="feffa-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feffa-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="feffa-111">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="feffa-111">**Minimum supported client**</span></span> | <span data-ttu-id="feffa-112">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="feffa-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="feffa-113">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="feffa-113">**Minimum supported server**</span></span> | <span data-ttu-id="feffa-114">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="feffa-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="feffa-115">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="feffa-115">**Header**</span></span> | <span data-ttu-id="feffa-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="feffa-116">Do.h</span></span> |
