---
description: Cada localidade tem um tipo de calendário padrão (tipo de dados CALTYPE) associado a ele. Uma localidade também pode ter um tipo de calendário alternativo. Para obter detalhes sobre os tipos de calendário, consulte informações de tipo de calendário.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Data e calendário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829798"
---
# <a name="date-and-calendar"></a><span data-ttu-id="cf2e0-105">Data e calendário</span><span class="sxs-lookup"><span data-stu-id="cf2e0-105">Date and Calendar</span></span>

<span data-ttu-id="cf2e0-106">Cada [localidade](locales-and-languages.md) tem um tipo de calendário padrão (tipo de dados CALTYPE) associado a ele.</span><span class="sxs-lookup"><span data-stu-id="cf2e0-106">Each [locale](locales-and-languages.md) has a default calendar type (data type CALTYPE) associated with it.</span></span> <span data-ttu-id="cf2e0-107">Uma localidade também pode ter um tipo de calendário alternativo.</span><span class="sxs-lookup"><span data-stu-id="cf2e0-107">A locale can also have an alternate calendar type.</span></span> <span data-ttu-id="cf2e0-108">Para obter detalhes sobre os tipos de calendário, consulte [informações de tipo de calendário](calendar-type-information.md).</span><span class="sxs-lookup"><span data-stu-id="cf2e0-108">For details of calendar types, see [Calendar Type Information](calendar-type-information.md).</span></span>

> [!Note]  
> <span data-ttu-id="cf2e0-109">Para usar um tipo de calendário alternativo para uma localidade, seu aplicativo deve definir a constante [ \_ IOPTIONALCALENDAR de localidade](locale-ioptionalcalendar.md) como o tipo de calendário alternativo para a localidade.</span><span class="sxs-lookup"><span data-stu-id="cf2e0-109">To use an alternate calendar type for a locale, your application must set the [LOCALE\_IOPTIONALCALENDAR](locale-ioptionalcalendar.md) constant to the alternate calendar type for the locale.</span></span>

 

<span data-ttu-id="cf2e0-110">A maioria das localidades usa o calendário gregoriano padrão e um número definido de formatos de data.</span><span class="sxs-lookup"><span data-stu-id="cf2e0-110">Most locales use the standard Gregorian calendar and a set number of date formats.</span></span> <span data-ttu-id="cf2e0-111">Essas opções padrão para formatos de data estão disponíveis para exibição usando a função [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) ou [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .</span><span class="sxs-lookup"><span data-stu-id="cf2e0-111">These default choices for date formats are available for display by using the [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) or [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) function.</span></span>

<span data-ttu-id="cf2e0-112">Algumas localidades exigem considerações especiais ao criar uma lista completa de opções de formato.</span><span class="sxs-lookup"><span data-stu-id="cf2e0-112">Some locales require special considerations when creating a complete list of format choices.</span></span> <span data-ttu-id="cf2e0-113">Algumas dessas localidades exigem que as cadeias de texto sejam inseridas na cadeia de caracteres de formato de data, enquanto outras exigem um método completamente diferente de computação dos valores.</span><span class="sxs-lookup"><span data-stu-id="cf2e0-113">Some of these locales require text strings to be inserted in the date format string, while others require a completely different method of computation of the values.</span></span> <span data-ttu-id="cf2e0-114">Um aplicativo resolve esses requisitos especiais pela adição de determinados tipos de informações de localidade e tipos de calendário.</span><span class="sxs-lookup"><span data-stu-id="cf2e0-114">An application addresses these special requirements by the addition of certain locale information types and calendar types.</span></span>

<span data-ttu-id="cf2e0-115">Para obter detalhes sobre como implementar datas e calendários em seus aplicativos, consulte [recuperando informações de data e hora](retrieving-time-and-date-information.md).</span><span class="sxs-lookup"><span data-stu-id="cf2e0-115">For details about implementing dates and calendars in your applications, see [Retrieving Time and Date Information](retrieving-time-and-date-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf2e0-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf2e0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf2e0-117">Sobre o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="cf2e0-117">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="cf2e0-118">Informações de tipo de calendário</span><span class="sxs-lookup"><span data-stu-id="cf2e0-118">Calendar Type Information</span></span>](calendar-type-information.md)
</dt> <dt>

[<span data-ttu-id="cf2e0-119">Recuperando informações de data e hora</span><span class="sxs-lookup"><span data-stu-id="cf2e0-119">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="cf2e0-120">**EnumDateFormatsEx**</span><span class="sxs-lookup"><span data-stu-id="cf2e0-120">**EnumDateFormatsEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[<span data-ttu-id="cf2e0-121">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="cf2e0-121">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



