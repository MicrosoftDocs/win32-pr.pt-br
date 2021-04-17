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
# <a name="ms-dos-date-and-time"></a>Data e hora do MS-DOS

A **data do MS-dos** e a hora do **MS-dos** são valores de 16 bits compactados que especificam o mês, o dia, o ano e a hora do dia em que um arquivo do MS-dos foi gravado pela última vez. O MS-DOS registra a data e a hora sempre que um aplicativo do MS-DOS cria ou grava em um arquivo. Os aplicativos do MS-DOS recuperam essa data e hora usando as funções do MS-DOS. Quando você usa a função [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) para recuperar os tempos de arquivo para arquivos que foram criados pelo MS-dos, **GetFileTime** converte automaticamente as datas e horários do MS-dos em horários baseados em UTC.

Se você encontrar uma data e hora do MS-DOS que não foram convertidas, poderá convertê-las em um horário baseado em UTC usando a função [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) . Essa função copia a data e a hora convertidas para uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . Você pode converter o valor de volta em uma data e hora do MS-DOS usando a função [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .

 

 
