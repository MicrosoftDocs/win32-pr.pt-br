---
description: Libera recursos usados pela função SdbGetMatchingExe.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: Função SdbReleaseMatchingExe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010147"
---
# <a name="sdbreleasematchingexe-function"></a><span data-ttu-id="401ed-103">Função SdbReleaseMatchingExe</span><span class="sxs-lookup"><span data-stu-id="401ed-103">SdbReleaseMatchingExe function</span></span>

<span data-ttu-id="401ed-104">Libera recursos usados pela função [**SdbGetMatchingExe**](sdbgetmatchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="401ed-104">Releases resources used by the [**SdbGetMatchingExe**](sdbgetmatchingexe.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="401ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="401ed-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a><span data-ttu-id="401ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="401ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="401ed-107">*hSDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="401ed-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="401ed-108">Um identificador para o banco de dados de Shim retornado pela função [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="401ed-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="401ed-109">*trExe* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="401ed-109">*trExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="401ed-110">O [**TAGREF**](tagref.md) retornado por [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span><span class="sxs-lookup"><span data-stu-id="401ed-110">The [**TAGREF**](tagref.md) returned by [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="401ed-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="401ed-111">Return value</span></span>

<span data-ttu-id="401ed-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="401ed-112">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="401ed-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="401ed-113">Requirements</span></span>



| <span data-ttu-id="401ed-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="401ed-114">Requirement</span></span> | <span data-ttu-id="401ed-115">Valor</span><span class="sxs-lookup"><span data-stu-id="401ed-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="401ed-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="401ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="401ed-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="401ed-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="401ed-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="401ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="401ed-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="401ed-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="401ed-120">DLL</span><span class="sxs-lookup"><span data-stu-id="401ed-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="401ed-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="401ed-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="401ed-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="401ed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401ed-123">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="401ed-123">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="401ed-124">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="401ed-124">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




