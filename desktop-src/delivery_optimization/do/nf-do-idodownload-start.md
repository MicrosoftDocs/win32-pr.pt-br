---
title: 'Método IDODownload:: Start'
description: Inicia ou retoma um download.
keywords:
- 'Método IDODownload:: Start'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105816042"
---
# <a name="idodownloadstart-method"></a><span data-ttu-id="6a298-104">Método IDODownload:: Start</span><span class="sxs-lookup"><span data-stu-id="6a298-104">IDODownload::Start method</span></span>

<span data-ttu-id="6a298-105">Inicia ou retoma um download, passando intervalos opcionais como um ponteiro para [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) estrutura.</span><span class="sxs-lookup"><span data-stu-id="6a298-105">Starts or resumes a download, passing optional ranges as a pointer to [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a298-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a298-106">Syntax</span></span>

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a><span data-ttu-id="6a298-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a298-107">Parameters</span></span>

`ranges`

<span data-ttu-id="6a298-108">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6a298-108">Optional.</span></span> <span data-ttu-id="6a298-109">Um ponteiro para uma estrutura de [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (para baixar apenas intervalos específicos do arquivo).</span><span class="sxs-lookup"><span data-stu-id="6a298-109">A pointer to a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure (to download only specific ranges of the file).</span></span> <span data-ttu-id="6a298-110">Passe `nullptr` para baixar o arquivo inteiro.</span><span class="sxs-lookup"><span data-stu-id="6a298-110">Pass `nullptr` to download the entire file.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a298-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6a298-111">Return Value</span></span>

<span data-ttu-id="6a298-112">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="6a298-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="6a298-113">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="6a298-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a298-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a298-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6a298-115">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="6a298-115">**Minimum supported client**</span></span> | <span data-ttu-id="6a298-116">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="6a298-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6a298-117">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="6a298-117">**Minimum supported server**</span></span> | <span data-ttu-id="6a298-118">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="6a298-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6a298-119">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="6a298-119">**Header**</span></span> | <span data-ttu-id="6a298-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="6a298-120">Do.h</span></span> |
