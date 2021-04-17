---
description: A data do MS-DOS e a hora do MS-DOS são valores de 16 bits compactados que especificam o mês, o dia, o ano e a hora do dia em que um arquivo do MS-DOS foi gravado pela última vez.
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: Data e hora do MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755533"
---
# <a name="ms-dos-date-and-time"></a><span data-ttu-id="bd0d0-103">Data e hora do MS-DOS</span><span class="sxs-lookup"><span data-stu-id="bd0d0-103">MS-DOS Date and Time</span></span>

<span data-ttu-id="bd0d0-104">A **data do MS-dos** e a hora do **MS-dos** são valores de 16 bits compactados que especificam o mês, o dia, o ano e a hora do dia em que um arquivo do MS-dos foi gravado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="bd0d0-104">**MS-DOS date** and **MS-DOS time** are packed 16-bit values that specify the month, day, year, and time of day an MS-DOS file was last written to.</span></span> <span data-ttu-id="bd0d0-105">O MS-DOS registra a data e a hora sempre que um aplicativo do MS-DOS cria ou grava em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bd0d0-105">MS-DOS records the date and time whenever an MS-DOS application creates or writes to a file.</span></span> <span data-ttu-id="bd0d0-106">Os aplicativos do MS-DOS recuperam essa data e hora usando as funções do MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="bd0d0-106">MS-DOS applications retrieve this date and time using MS-DOS functions.</span></span> <span data-ttu-id="bd0d0-107">Quando você usa a função [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) para recuperar os tempos de arquivo para arquivos que foram criados pelo MS-dos, **GetFileTime** converte automaticamente as datas e horários do MS-dos em horários baseados em UTC.</span><span class="sxs-lookup"><span data-stu-id="bd0d0-107">When you use the [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) function to retrieve the file times for files that were created by MS-DOS, **GetFileTime** automatically converts MS-DOS dates and times to UTC-based times.</span></span>

<span data-ttu-id="bd0d0-108">Se você encontrar uma data e hora do MS-DOS que não foram convertidas, poderá convertê-las em um horário baseado em UTC usando a função [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) .</span><span class="sxs-lookup"><span data-stu-id="bd0d0-108">If you encounter an MS-DOS date and time that has not been converted, you can convert it to a UTC-based time by using the [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) function.</span></span> <span data-ttu-id="bd0d0-109">Essa função copia a data e a hora convertidas para uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="bd0d0-109">This function copies the converted date and time to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="bd0d0-110">Você pode converter o valor de volta em uma data e hora do MS-DOS usando a função [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .</span><span class="sxs-lookup"><span data-stu-id="bd0d0-110">You can convert the value back to an MS-DOS date and time by using the [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) function.</span></span>

 

 
