---
description: Contém a data de fabricação de uma bateria.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: Estrutura de BATTERY_MANUFACTURE_DATE (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758926"
---
# <a name="battery_manufacture_date-structure"></a><span data-ttu-id="179f7-103">Estrutura de data de \_ fabricação da bateria \_</span><span class="sxs-lookup"><span data-stu-id="179f7-103">BATTERY\_MANUFACTURE\_DATE structure</span></span>

<span data-ttu-id="179f7-104">Contém a data de fabricação de uma bateria.</span><span class="sxs-lookup"><span data-stu-id="179f7-104">Contains the date of manufacture of a battery.</span></span> <span data-ttu-id="179f7-105">Essa estrutura é usada pela estrutura [**de \_ \_ informações de consulta de bateria**](battery-query-information-str.md) quando o nível de informações BatteryManufactureDate é solicitado.</span><span class="sxs-lookup"><span data-stu-id="179f7-105">This structure is used by the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure when the BatteryManufactureDate information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="179f7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="179f7-106">Syntax</span></span>


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a><span data-ttu-id="179f7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="179f7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="179f7-108">**Day**</span><span class="sxs-lookup"><span data-stu-id="179f7-108">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="179f7-109">O dia do mês de fabricação, no intervalo de 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="179f7-109">The day of the month of manufacture, in the range 1 to 31.</span></span> <span data-ttu-id="179f7-110">Apesar do tipo de dados, esse não é um valor codificado em ASCII.</span><span class="sxs-lookup"><span data-stu-id="179f7-110">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="179f7-111">É um byte não assinado.</span><span class="sxs-lookup"><span data-stu-id="179f7-111">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="179f7-112">**Mês**</span><span class="sxs-lookup"><span data-stu-id="179f7-112">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="179f7-113">O mês de fabricação, no intervalo de 1 (Janeiro) a 12 (Dezembro).</span><span class="sxs-lookup"><span data-stu-id="179f7-113">The month of manufacture, in the range 1 (January) to 12 (December).</span></span> <span data-ttu-id="179f7-114">Apesar do tipo de dados, esse não é um valor codificado em ASCII.</span><span class="sxs-lookup"><span data-stu-id="179f7-114">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="179f7-115">É um byte não assinado.</span><span class="sxs-lookup"><span data-stu-id="179f7-115">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="179f7-116">**Year**</span><span class="sxs-lookup"><span data-stu-id="179f7-116">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="179f7-117">O ano de fabricação.</span><span class="sxs-lookup"><span data-stu-id="179f7-117">The year of manufacture.</span></span> <span data-ttu-id="179f7-118">Normalmente, isso estará no intervalo de 1900-2100.</span><span class="sxs-lookup"><span data-stu-id="179f7-118">This will typically be in the range 1900-2100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="179f7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="179f7-119">Remarks</span></span>

<span data-ttu-id="179f7-120">A data é codificada no formato Gregoriano ou do calendário ocidental.</span><span class="sxs-lookup"><span data-stu-id="179f7-120">The date is encoded in the Gregorian or western calendar format.</span></span>

## <a name="requirements"></a><span data-ttu-id="179f7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="179f7-121">Requirements</span></span>



| <span data-ttu-id="179f7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="179f7-122">Requirement</span></span> | <span data-ttu-id="179f7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="179f7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="179f7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="179f7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="179f7-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="179f7-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="179f7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="179f7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="179f7-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="179f7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="179f7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="179f7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="179f7-129"><dt>Poclass. h; </dt> <dt>Batclass. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="179f7-129"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="179f7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="179f7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="179f7-131">**\_informações de consulta de bateria \_**</span><span class="sxs-lookup"><span data-stu-id="179f7-131">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="179f7-132">**\_informações de \_ consulta da bateria do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="179f7-132">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




