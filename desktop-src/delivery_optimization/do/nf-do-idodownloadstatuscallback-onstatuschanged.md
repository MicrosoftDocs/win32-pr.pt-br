---
title: 'Método IDODownloadStatusCallback:: OnStatusChange'
description: O chama sua implementação desse método sempre que um status de download for alterado.
keywords:
- 'Método IDODownloadStatusCallback:: OnStatusChange'
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104006950"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a><span data-ttu-id="88b2b-104">Método IDODownloadStatusCallback:: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="88b2b-104">IDODownloadStatusCallback::OnStatusChange method</span></span>

<span data-ttu-id="88b2b-105">O chama sua implementação desse método sempre que um status de download for alterado.</span><span class="sxs-lookup"><span data-stu-id="88b2b-105">DO calls your implementation of this method any time a download status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b2b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88b2b-106">Syntax</span></span>

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="88b2b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88b2b-107">Parameters</span></span>

`download`

<span data-ttu-id="88b2b-108">Um ponteiro para a interface **IDODownload** cujo status mudou.</span><span class="sxs-lookup"><span data-stu-id="88b2b-108">An pointer to the **IDODownload** interface whose status changed.</span></span>

`status`

<span data-ttu-id="88b2b-109">Um ponteiro para uma estrutura de **DO_DOWNLOAD_STATUS** que contém o status do download.</span><span class="sxs-lookup"><span data-stu-id="88b2b-109">A pointer to a **DO_DOWNLOAD_STATUS** structure containing the download's status.</span></span>

## <a name="return-value"></a><span data-ttu-id="88b2b-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="88b2b-110">Return Value</span></span>

<span data-ttu-id="88b2b-111">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="88b2b-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="88b2b-112">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="88b2b-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="88b2b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88b2b-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="88b2b-114">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="88b2b-114">**Minimum supported client**</span></span> | <span data-ttu-id="88b2b-115">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="88b2b-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="88b2b-116">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="88b2b-116">**Minimum supported server**</span></span> | <span data-ttu-id="88b2b-117">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="88b2b-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="88b2b-118">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="88b2b-118">**Header**</span></span> | <span data-ttu-id="88b2b-119">Do. h</span><span class="sxs-lookup"><span data-stu-id="88b2b-119">Do.h</span></span> |
