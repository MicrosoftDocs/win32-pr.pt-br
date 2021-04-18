---
title: Estrutura WMDMDATETIME
description: A estrutura WMDMDATETIME contém uma data e hora do dia.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Estrutura WMDMDATETIME Windows Media Gerenciador de Dispositivos
- Ponteiro de estrutura PWMDMDATETIME Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781069"
---
# <a name="wmdmdatetime-structure"></a><span data-ttu-id="2d4ae-105">Estrutura WMDMDATETIME</span><span class="sxs-lookup"><span data-stu-id="2d4ae-105">WMDMDATETIME structure</span></span>

<span data-ttu-id="2d4ae-106">A estrutura **WMDMDATETIME** contém uma data e hora do dia.</span><span class="sxs-lookup"><span data-stu-id="2d4ae-106">The **WMDMDATETIME** structure contains a date and time of day.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d4ae-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d4ae-107">Syntax</span></span>


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a><span data-ttu-id="2d4ae-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2d4ae-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2d4ae-109">**Wano**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-109">**wYear**</span></span>
</dt> <dd>

<span data-ttu-id="2d4ae-110">O Word que contém o ano de quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="2d4ae-110">Word containing the four-digit year.</span></span>

</dd> <dt>

<span data-ttu-id="2d4ae-111">**Wmês**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-111">**wMonth**</span></span>
</dt> <dd>

<span data-ttu-id="2d4ae-112">O Word que contém o mês (1-12).</span><span class="sxs-lookup"><span data-stu-id="2d4ae-112">Word containing the month (1-12).</span></span>

</dd> <dt>

<span data-ttu-id="2d4ae-113">**WDIA**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-113">**wDay**</span></span>
</dt> <dd>

<span data-ttu-id="2d4ae-114">O Word que contém o dia do mês (1-31).</span><span class="sxs-lookup"><span data-stu-id="2d4ae-114">Word containing the day of the month (1-31).</span></span>

</dd> <dt>

<span data-ttu-id="2d4ae-115">**Whora**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-115">**wHour**</span></span>
</dt> <dd>

<span data-ttu-id="2d4ae-116">O Word que contém a hora (0-23).</span><span class="sxs-lookup"><span data-stu-id="2d4ae-116">Word containing the hour (0-23).</span></span>

</dd> <dt>

<span data-ttu-id="2d4ae-117">**Wminuto**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-117">**wMinute**</span></span>
</dt> <dd>

<span data-ttu-id="2d4ae-118">O Word que contém o minuto (0-59).</span><span class="sxs-lookup"><span data-stu-id="2d4ae-118">Word containing the minute (0-59).</span></span>

</dd> <dt>

<span data-ttu-id="2d4ae-119">**Wsegundo**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-119">**wSecond**</span></span>
</dt> <dd>

<span data-ttu-id="2d4ae-120">O Word que contém o segundo (0-59).</span><span class="sxs-lookup"><span data-stu-id="2d4ae-120">Word containing the second (0-59).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d4ae-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d4ae-121">Requirements</span></span>



| <span data-ttu-id="2d4ae-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d4ae-122">Requirement</span></span> | <span data-ttu-id="2d4ae-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2d4ae-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2d4ae-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d4ae-124">Header</span></span><br/> | <dl> <span data-ttu-id="2d4ae-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d4ae-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d4ae-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d4ae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d4ae-127">**IMDSPStorage:: GetDate**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-127">**IMDSPStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[<span data-ttu-id="2d4ae-128">**IWMDMStorage:: GetDate**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-128">**IWMDMStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[<span data-ttu-id="2d4ae-129">**WMDMRIGHTS**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-129">**WMDMRIGHTS**</span></span>](wmdmrights.md)
</dt> <dt>

[<span data-ttu-id="2d4ae-130">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="2d4ae-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





