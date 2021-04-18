---
description: Define os intervalos de data e hora com um formato semelhante à sintaxe de data e hora, dividindo a cadeia de caracteres nos campos de dias, horas, minutos, segundos e microssegundos.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Formato do intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750090"
---
# <a name="interval-format"></a><span data-ttu-id="93c5d-103">Formato do intervalo</span><span class="sxs-lookup"><span data-stu-id="93c5d-103">Interval Format</span></span>

<span data-ttu-id="93c5d-104">O WMI define os intervalos de data e hora com um formato semelhante à sintaxe de data e hora, dividindo a cadeia de caracteres nos campos de dias, horas, minutos, segundos e microssegundos.</span><span class="sxs-lookup"><span data-stu-id="93c5d-104">WMI defines date-time intervals with a format similar to the date and time syntax by breaking the string into the fields for days, hours, minutes, seconds, and microseconds.</span></span>

<span data-ttu-id="93c5d-105">O exemplo a seguir mostra o formato de um intervalo de data e hora.</span><span class="sxs-lookup"><span data-stu-id="93c5d-105">The following example shows the format of a date-time interval.</span></span>

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

<span data-ttu-id="93c5d-106">A tabela a seguir lista os campos do intervalo de data e hora.</span><span class="sxs-lookup"><span data-stu-id="93c5d-106">The following table lists the fields of the date-time interval.</span></span>



| <span data-ttu-id="93c5d-107">Campo</span><span class="sxs-lookup"><span data-stu-id="93c5d-107">Field</span></span>    | <span data-ttu-id="93c5d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="93c5d-108">Description</span></span>                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c5d-109">dddddddd</span><span class="sxs-lookup"><span data-stu-id="93c5d-109">dddddddd</span></span> | <span data-ttu-id="93c5d-110">Oito dígitos que representam um número de dias (00000000 a 99999999).</span><span class="sxs-lookup"><span data-stu-id="93c5d-110">Eight digits that represent a number of days (00000000 through 99999999).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="93c5d-111">HH</span><span class="sxs-lookup"><span data-stu-id="93c5d-111">HH</span></span>       | <span data-ttu-id="93c5d-112">A hora de dois dígitos do dia que usa o relógio de 24 horas (00 a 23).</span><span class="sxs-lookup"><span data-stu-id="93c5d-112">Two-digit hour of the day that uses the 24-hour clock (00 through 23).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="93c5d-113">MM</span><span class="sxs-lookup"><span data-stu-id="93c5d-113">MM</span></span>       | <span data-ttu-id="93c5d-114">Minuto de dois dígitos na hora (00 a 59).</span><span class="sxs-lookup"><span data-stu-id="93c5d-114">Two-digit minute in the hour (00 through 59).</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="93c5d-115">SS</span><span class="sxs-lookup"><span data-stu-id="93c5d-115">SS</span></span>       | <span data-ttu-id="93c5d-116">Número de segundos de dois dígitos no minuto (00 a 59).</span><span class="sxs-lookup"><span data-stu-id="93c5d-116">Two-digit number of seconds in the minute (00 through 59).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="93c5d-117">mmmmmm</span><span class="sxs-lookup"><span data-stu-id="93c5d-117">mmmmmm</span></span>   | <span data-ttu-id="93c5d-118">Número de seis dígitos de microssegundos no segundo (000000 a 999999).</span><span class="sxs-lookup"><span data-stu-id="93c5d-118">Six-digit number of microseconds in the second (000000 through 999999).</span></span> <span data-ttu-id="93c5d-119">Sua implementação não é necessária para dar suporte à avaliação usando esse campo, mas esse campo sempre deve estar presente para preservar a natureza de comprimento fixo da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="93c5d-119">Your implementation is not required to support evaluation using this field, but this field must always be present to preserve the fixed-length nature of the string.</span></span> |



 

<span data-ttu-id="93c5d-120">Os intervalos sempre têm um ": 000" à direita como os últimos quatro caracteres.</span><span class="sxs-lookup"><span data-stu-id="93c5d-120">Intervals always have a trailing ":000" as the last four characters.</span></span> <span data-ttu-id="93c5d-121">Além disso, diferentemente da data e hora, você não pode usar asteriscos para indicar campos não utilizados.</span><span class="sxs-lookup"><span data-stu-id="93c5d-121">Further, unlike the date and time, you cannot use asterisks to indicate unused fields.</span></span> <span data-ttu-id="93c5d-122">Além disso, todas as propriedades do [tipo \_ data e hora CIM](cim-datetime.md) que representam intervalos devem ser marcadas com o qualificador padrão de [subtipo](standard-wmi-qualifiers.md) , com o qualificador definido como "Interval".</span><span class="sxs-lookup"><span data-stu-id="93c5d-122">In addition, all properties of type [CIM\_DATETIME](cim-datetime.md) that represent intervals must be marked with the [SubType](standard-wmi-qualifiers.md) standard qualifier, with the qualifier set to "interval".</span></span>

<span data-ttu-id="93c5d-123">A cadeia de caracteres a seguir representa um intervalo de 1 dia, 12 horas, 0 minutos e 32 segundos.</span><span class="sxs-lookup"><span data-stu-id="93c5d-123">The following string represents an interval of 1 day, 12 hours, 0 minutes, and 32 seconds.</span></span>

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a><span data-ttu-id="93c5d-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93c5d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93c5d-125">Formato de data e hora</span><span class="sxs-lookup"><span data-stu-id="93c5d-125">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="93c5d-126">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="93c5d-126">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="93c5d-127">\_data e hora CIM</span><span class="sxs-lookup"><span data-stu-id="93c5d-127">CIM\_DATETIME</span></span>](cim-datetime.md)
</dt> </dl>

 

 



