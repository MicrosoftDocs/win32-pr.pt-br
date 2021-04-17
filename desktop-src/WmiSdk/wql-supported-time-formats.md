---
description: Descreve os formatos de tempo com suporte para uso na cláusula WHERE do WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: Formatos de hora WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812035"
---
# <a name="wql-supported-time-formats"></a><span data-ttu-id="d5345-103">Formatos de hora WQL-Supported</span><span class="sxs-lookup"><span data-stu-id="d5345-103">WQL-Supported Time Formats</span></span>

<span data-ttu-id="d5345-104">Além do formato de data e hora do WMI, os seguintes formatos de datas têm suporte para uso na cláusula WHERE do WQL.</span><span class="sxs-lookup"><span data-stu-id="d5345-104">In addition to the WMI DATETIME format, the following date formats are supported for use in the WQL WHERE clause.</span></span>



| <span data-ttu-id="d5345-105">Formatar</span><span class="sxs-lookup"><span data-stu-id="d5345-105">Format</span></span>                                    | <span data-ttu-id="d5345-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5345-106">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5345-107">HH \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="d5345-107">hh\[ \]{AP}M</span></span><br/>                   | <span data-ttu-id="d5345-108">Hora, conforme mostrado em um relógio de doze horas e na designação AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="d5345-108">Hour as shown on a twelve-hour clock, and AM or PM designation.</span></span><br/> <span data-ttu-id="d5345-109">4 PM</span><span class="sxs-lookup"><span data-stu-id="d5345-109">4 PM</span></span><br/>                                                                                                             |
| <span data-ttu-id="d5345-110">hh:mm</span><span class="sxs-lookup"><span data-stu-id="d5345-110">hh:mm</span></span><br/>                          | <span data-ttu-id="d5345-111">Hora e minutos delimitados por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="d5345-111">Colon-delimited hour and minutes.</span></span> <span data-ttu-id="d5345-112">Nenhuma designação AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="d5345-112">No AM or PM designation.</span></span><br/> <span data-ttu-id="d5345-113">3:23</span><span class="sxs-lookup"><span data-stu-id="d5345-113">3:23</span></span><br/>                                                                                                                  |
| <span data-ttu-id="d5345-114">hh: mm \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="d5345-114">hh:mm\[ \]{AP}M</span></span><br/>                | <span data-ttu-id="d5345-115">Hora e minutos delimitados por dois-pontos, espaço opcional e designação AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="d5345-115">Colon-delimited hour and minutes, optional space, and AM or PM designation.</span></span><br/> <span data-ttu-id="d5345-116">3:23 AM</span><span class="sxs-lookup"><span data-stu-id="d5345-116">3:23 AM</span></span><br/>                                                                                              |
| <span data-ttu-id="d5345-117">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="d5345-117">hh:mm:ss</span></span><br/>                       | <span data-ttu-id="d5345-118">Hora delimitada por dois-pontos, minutos e segundos.</span><span class="sxs-lookup"><span data-stu-id="d5345-118">Colon-delimited hour, minutes and seconds.</span></span> <span data-ttu-id="d5345-119">Nenhuma designação AM/PM.</span><span class="sxs-lookup"><span data-stu-id="d5345-119">No AM/PM designation.</span></span><br/> <span data-ttu-id="d5345-120">3:23:00</span><span class="sxs-lookup"><span data-stu-id="d5345-120">3:23:00</span></span><br/>                                                                                                         |
| <span data-ttu-id="d5345-121">hh: mm: SS \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="d5345-121">hh:mm:ss\[ \]{AP}M</span></span><br/>             | <span data-ttu-id="d5345-122">Hora delimitada por dois-pontos, minutos e segundos, espaço opcional e designação AM/PM.</span><span class="sxs-lookup"><span data-stu-id="d5345-122">Colon-delimited hour, minutes and seconds, optional space, and AM/PM designation.</span></span><br/> <span data-ttu-id="d5345-123">3:23:13H</span><span class="sxs-lookup"><span data-stu-id="d5345-123">3:23:00PM</span></span><br/>                                                                                      |
| <span data-ttu-id="d5345-124">hh: mm: SS: uuu</span><span class="sxs-lookup"><span data-stu-id="d5345-124">hh:mm:ss:uuu</span></span><br/>                   | <span data-ttu-id="d5345-125">Hora delimitada por dois-pontos, minutos e segundos e deslocamento de três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC.</span><span class="sxs-lookup"><span data-stu-id="d5345-125">Colon-delimited hour, minutes and seconds, and three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                                    |
| <span data-ttu-id="d5345-126">hh: mm: SS: u \[ \[ \] u \] u</span><span class="sxs-lookup"><span data-stu-id="d5345-126">hh:mm:ss:\[\[u\]u\]u</span></span><br/>           | <span data-ttu-id="d5345-127">Hora delimitada por dois-pontos, minutos e segundos; e um deslocamento de um, dois ou três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC.</span><span class="sxs-lookup"><span data-stu-id="d5345-127">Colon-delimited hour, minutes and seconds; and one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                       |
| <span data-ttu-id="d5345-128">hh: mm: SS: uuu \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="d5345-128">hh:mm:ss:uuu\[ \]{AP}M</span></span><br/>         | <span data-ttu-id="d5345-129">Hora delimitada por dois-pontos, minutos e segundos, deslocamento de três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC e a designação AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="d5345-129">Colon-delimited hour, minutes and seconds, three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC, and AM or PM designation.</span></span><br/>              |
| <span data-ttu-id="d5345-130">hh: mm: SS: u u u \[ \[ \] \] \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="d5345-130">hh:mm:ss:\[\[u\]u\]u\[ \]{AP}M</span></span><br/> | <span data-ttu-id="d5345-131">Hora delimitada por dois-pontos, minutos e segundos; um deslocamento de um, dois ou três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC; e a designação AM ou PM.</span><span class="sxs-lookup"><span data-stu-id="d5345-131">Colon-delimited hour, minutes and seconds; one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC; and AM or PM designation.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="d5345-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5345-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5345-133">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="d5345-133">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




