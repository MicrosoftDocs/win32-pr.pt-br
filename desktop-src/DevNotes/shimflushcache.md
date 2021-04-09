---
description: Libera o cache do banco de dados Shim. Essa função deve ser chamada após a instalação de um novo banco de dados de Shim.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: Função ShimFlushCache
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010082"
---
# <a name="shimflushcache-function"></a><span data-ttu-id="b7792-104">Função ShimFlushCache</span><span class="sxs-lookup"><span data-stu-id="b7792-104">ShimFlushCache function</span></span>

<span data-ttu-id="b7792-105">Libera o cache do banco de dados Shim.</span><span class="sxs-lookup"><span data-stu-id="b7792-105">Flushes the shim database cache.</span></span> <span data-ttu-id="b7792-106">Essa função deve ser chamada após a instalação de um novo banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="b7792-106">This function should be called after installing a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7792-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7792-107">Syntax</span></span>


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="b7792-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7792-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7792-109">*HWND* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7792-109">*hwnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7792-110">Não utilizado deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="b7792-110">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="b7792-111">*HINSTANCE* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7792-111">*hInstance* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7792-112">Não utilizado deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="b7792-112">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="b7792-113">*lpszCmdLine* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7792-113">*lpszCmdLine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7792-114">Não utilizado deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="b7792-114">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="b7792-115">*nCmdShow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7792-115">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7792-116">Não utilizado deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="b7792-116">Unused; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7792-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7792-117">Return value</span></span>

<span data-ttu-id="b7792-118">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="b7792-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7792-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7792-119">Remarks</span></span>

<span data-ttu-id="b7792-120">O chamador deve ser um administrador.</span><span class="sxs-lookup"><span data-stu-id="b7792-120">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7792-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7792-121">Requirements</span></span>



| <span data-ttu-id="b7792-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7792-122">Requirement</span></span> | <span data-ttu-id="b7792-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b7792-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7792-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7792-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b7792-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7792-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b7792-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7792-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b7792-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7792-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b7792-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b7792-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7792-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7792-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7792-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7792-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7792-131">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="b7792-131">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
</dt> </dl>

 

 




