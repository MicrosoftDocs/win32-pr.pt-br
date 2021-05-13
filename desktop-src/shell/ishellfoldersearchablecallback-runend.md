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
ms.openlocfilehash: c23d461fdbd175a80a8fa94fcc238f6cf2f89869
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842817"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="c4683-103">Método IShellFolderSearchableCallback:: RunEnd</span><span class="sxs-lookup"><span data-stu-id="c4683-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="c4683-104">Indica que uma pesquisa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="c4683-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4683-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4683-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="c4683-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4683-107">*dwReserved* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4683-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4683-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c4683-108">Type: **DWORD**</span></span>

<span data-ttu-id="c4683-109">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c4683-109">Reserved.</span></span> <span data-ttu-id="c4683-110">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="c4683-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4683-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4683-111">Return value</span></span>

<span data-ttu-id="c4683-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4683-112">Type: **HRESULT**</span></span>

<span data-ttu-id="c4683-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4683-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4683-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4683-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4683-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4683-115">Requirements</span></span>



| <span data-ttu-id="c4683-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4683-116">Requirement</span></span> | <span data-ttu-id="c4683-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c4683-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4683-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4683-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c4683-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c4683-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c4683-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4683-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c4683-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c4683-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4683-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c4683-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4683-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4683-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




