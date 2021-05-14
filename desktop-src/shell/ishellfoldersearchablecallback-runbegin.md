---
description: Indica que uma pesquisa foi iniciada.
title: Método IShellFolderSearchableCallback::RunBegin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 953bf54ff64cf41724ce0dfabd064f9c7b980cc6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842807"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a><span data-ttu-id="4e1b3-103">Método IShellFolderSearchableCallback::RunBegin</span><span class="sxs-lookup"><span data-stu-id="4e1b3-103">IShellFolderSearchableCallback::RunBegin method</span></span>

<span data-ttu-id="4e1b3-104">Indica que uma pesquisa foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="4e1b3-104">Indicates that a search was started.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e1b3-105">Syntax</span></span>


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="4e1b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e1b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1b3-107">*dwReserved* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="4e1b3-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1b3-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4e1b3-108">Type: **DWORD**</span></span>

<span data-ttu-id="4e1b3-109">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4e1b3-109">Reserved.</span></span> <span data-ttu-id="4e1b3-110">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="4e1b3-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1b3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e1b3-111">Return value</span></span>

<span data-ttu-id="4e1b3-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4e1b3-112">Type: **HRESULT**</span></span>

<span data-ttu-id="4e1b3-113">Se esse método for bem-sucedido, ele **retornará S \_ OK.**</span><span class="sxs-lookup"><span data-stu-id="4e1b3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e1b3-114">Caso contrário, ele retornará um **código de erro HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="4e1b3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e1b3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e1b3-115">Remarks</span></span>

<span data-ttu-id="4e1b3-116">Em resposta a esse retorno de chamada, o aplicativo pode habilitar **o botão** Cancelar, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="4e1b3-116">In response to this callback, the application may enable the **Cancel** button, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1b3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e1b3-117">Requirements</span></span>



| <span data-ttu-id="4e1b3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e1b3-118">Requirement</span></span> | <span data-ttu-id="4e1b3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4e1b3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1b3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e1b3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1b3-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e1b3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4e1b3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e1b3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1b3-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e1b3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4e1b3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4e1b3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e1b3-125"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e1b3-125"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




