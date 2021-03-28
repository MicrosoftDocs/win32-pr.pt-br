---
description: Indica que uma pesquisa foi concluída.
title: 'Método IShellFolderSearchableCallback:: RunEnd'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: 73155e65f4b6edb4a4b4b9b0d52ab5b042fa68b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988851"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="b32d0-103">Método IShellFolderSearchableCallback:: RunEnd</span><span class="sxs-lookup"><span data-stu-id="b32d0-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="b32d0-104">Indica que uma pesquisa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="b32d0-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b32d0-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="b32d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b32d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b32d0-107">*dwReserved* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b32d0-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b32d0-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b32d0-108">Type: **DWORD**</span></span>

<span data-ttu-id="b32d0-109">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b32d0-109">Reserved.</span></span> <span data-ttu-id="b32d0-110">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="b32d0-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b32d0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b32d0-111">Return value</span></span>

<span data-ttu-id="b32d0-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b32d0-112">Type: **HRESULT**</span></span>

<span data-ttu-id="b32d0-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b32d0-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b32d0-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b32d0-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b32d0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b32d0-115">Requirements</span></span>



| <span data-ttu-id="b32d0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b32d0-116">Requirement</span></span> | <span data-ttu-id="b32d0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b32d0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b32d0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b32d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b32d0-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b32d0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b32d0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b32d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b32d0-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b32d0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b32d0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b32d0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b32d0-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b32d0-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




