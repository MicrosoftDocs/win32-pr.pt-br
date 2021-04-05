---
description: Libera os dados de atributo de arquivo especificados.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Função SdbFreeFileAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646196"
---
# <a name="sdbfreefileattributes-function"></a><span data-ttu-id="747b3-103">Função SdbFreeFileAttributes</span><span class="sxs-lookup"><span data-stu-id="747b3-103">SdbFreeFileAttributes function</span></span>

<span data-ttu-id="747b3-104">Libera os dados de atributo de arquivo especificados.</span><span class="sxs-lookup"><span data-stu-id="747b3-104">Frees the specified file attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="747b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="747b3-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="747b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="747b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747b3-107">*pFileAttributes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="747b3-107">*pFileAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="747b3-108">Uma estrutura [**ATTRINFO**](attrinfo.md) retornada pela função [**SdbGetFileAttributes**](sdbgetfileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="747b3-108">An [**ATTRINFO**](attrinfo.md) structure returned by the [**SdbGetFileAttributes**](sdbgetfileattributes.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747b3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="747b3-109">Return value</span></span>

<span data-ttu-id="747b3-110">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="747b3-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="747b3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="747b3-111">Requirements</span></span>



| <span data-ttu-id="747b3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="747b3-112">Requirement</span></span> | <span data-ttu-id="747b3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="747b3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="747b3-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="747b3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="747b3-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="747b3-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="747b3-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="747b3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="747b3-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="747b3-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="747b3-118">DLL</span><span class="sxs-lookup"><span data-stu-id="747b3-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="747b3-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="747b3-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747b3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="747b3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747b3-121">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="747b3-121">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




