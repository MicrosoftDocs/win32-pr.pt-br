---
description: Recupera o nome de exibição da marca especificada.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: Função SdbTagToString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456975"
---
# <a name="sdbtagtostring-function"></a><span data-ttu-id="6d409-103">Função SdbTagToString</span><span class="sxs-lookup"><span data-stu-id="6d409-103">SdbTagToString function</span></span>

<span data-ttu-id="6d409-104">Recupera o nome de exibição da marca especificada.</span><span class="sxs-lookup"><span data-stu-id="6d409-104">Retrieves the display name of the specified TAG.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d409-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d409-105">Syntax</span></span>


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a><span data-ttu-id="6d409-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d409-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d409-107">*marca* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="6d409-107">*tag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d409-108">A marca.</span><span class="sxs-lookup"><span data-stu-id="6d409-108">The TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d409-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d409-109">Return value</span></span>

<span data-ttu-id="6d409-110">A função retorna um ponteiro para a cadeia de caracteres terminada em nulo ou "InvalidTag".</span><span class="sxs-lookup"><span data-stu-id="6d409-110">The function returns a pointer to the null-terminated string or "InvalidTag".</span></span>

## <a name="requirements"></a><span data-ttu-id="6d409-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d409-111">Requirements</span></span>



| <span data-ttu-id="6d409-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d409-112">Requirement</span></span> | <span data-ttu-id="6d409-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6d409-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d409-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d409-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6d409-115">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6d409-115">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6d409-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d409-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6d409-117">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d409-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6d409-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6d409-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d409-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d409-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d409-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d409-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d409-121">**Tags**</span><span class="sxs-lookup"><span data-stu-id="6d409-121">**TAG**</span></span>](tag.md)
</dt> </dl>

 

 




