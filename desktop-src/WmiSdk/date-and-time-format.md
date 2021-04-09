---
description: Descreve o formato de data e hora do modelo CIM (CIM) usado pelo WMI. Esse formato é independente de localidade, de modo que os scripts que usam DATETIME podem ser executados em vários fusos horários.
ms.assetid: be239bf8-88a3-47bc-ae4f-49a5195e7a7d
ms.tgt_platform: multiple
title: Formato de data e hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e8f97930efa33942fe87b2109aa7cd7ba9d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091376"
---
# <a name="date-and-time-format"></a><span data-ttu-id="a238a-104">Formato de data e hora</span><span class="sxs-lookup"><span data-stu-id="a238a-104">Date and Time Format</span></span>

<span data-ttu-id="a238a-105">O WMI usa os formatos de data e hora definidos pela especificação de CIM ([DMTF.org](https://www.dmtf.org/)) modelo CIM (Distributed Management Task Force).</span><span class="sxs-lookup"><span data-stu-id="a238a-105">WMI uses the date and time formats defined by the Distributed Management Task Force ([DMTF.org](https://www.dmtf.org/)) Common Information Model (CIM) specification.</span></span>

<span data-ttu-id="a238a-106">O formato de **\_ data e hora CIM** é implementado no Microsoft [formato MOF (MOF)](managed-object-format--mof-.md) pelo tipo de dados MOF [DateTime](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="a238a-106">The **CIM\_DATETIME** format is implemented in the Microsoft [Managed Object Format (MOF)](managed-object-format--mof-.md) by the [DATETIME](datetime.md) MOF datatype.</span></span> <span data-ttu-id="a238a-107">Os formatos de data e hora também podem expressar um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a238a-107">The date and time formats can also express an interval of time.</span></span>

<span data-ttu-id="a238a-108">Para obter mais informações sobre formatos WMI, consulte [CIM \_ DateTime](cim-datetime.md) e [formato de intervalo](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="a238a-108">For more information about WMI formats, see [CIM\_DATETIME](cim-datetime.md) and [Interval Format](interval-format.md).</span></span>

<span data-ttu-id="a238a-109">Para obter mais informações sobre como converter de e para o formato de data e hora do WMI, consulte [**SWbemDateTime**](swbemdatetime.md) e o artigo sobre o TechNet ScriptCenter [sobre o tempo (Ah e sobre datas também)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="a238a-109">For more information about converting to and from the WMI DATETIME format, see [**SWbemDateTime**](swbemdatetime.md) and the article on TechNet ScriptCenter [It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a238a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a238a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a238a-111">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="a238a-111">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



