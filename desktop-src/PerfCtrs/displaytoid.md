---
description: A tabela DisplayToID relaciona a cadeia de caracteres amigável exibida pelo monitor do sistema ao GUID armazenado nas outras tabelas.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757090"
---
# <a name="displaytoid"></a><span data-ttu-id="e138f-103">DisplayToID</span><span class="sxs-lookup"><span data-stu-id="e138f-103">DisplayToID</span></span>

<span data-ttu-id="e138f-104">A tabela **DisplayToID** relaciona a cadeia de caracteres amigável exibida pelo monitor do sistema ao GUID armazenado nas outras tabelas.</span><span class="sxs-lookup"><span data-stu-id="e138f-104">The **DisplayToID** table relates the user-friendly string displayed by the System Monitor to the GUID stored in the other tables.</span></span>

<span data-ttu-id="e138f-105">A tabela **DisplayToID** define os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="e138f-105">The **DisplayToID** table defines the following fields:</span></span>

-   <span data-ttu-id="e138f-106">**GUID:** Identificador exclusivo gerado para um log.</span><span class="sxs-lookup"><span data-stu-id="e138f-106">**GUID:** Unique identifier generated for a log.</span></span> <span data-ttu-id="e138f-107">Este campo é a chave primária desta tabela.</span><span class="sxs-lookup"><span data-stu-id="e138f-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="e138f-108">**RunId:** Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="e138f-108">**RunID:** Reserved for internal use.</span></span>
-   <span data-ttu-id="e138f-109">**DisplayString:** Nome do arquivo de log, conforme exibido no monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="e138f-109">**DisplayString:** Name of the log file as displayed in the System Monitor.</span></span>
-   <span data-ttu-id="e138f-110">**LogStartTime:** Hora em que o processo de log foi iniciado no formato aaaa-mm-dd hh: mm: SS: nnn.</span><span class="sxs-lookup"><span data-stu-id="e138f-110">**LogStartTime:** Time the logging process started in yyyy-mm-dd hh:mm:ss:nnn format.</span></span>
-   <span data-ttu-id="e138f-111">**LogStopTime:** Tempo que o processo de log parou no formato aaaa-mm-dd hh: mm: SS: nnn.</span><span class="sxs-lookup"><span data-stu-id="e138f-111">**LogStopTime:** Time the logging process stopped in yyyy-mm-dd hh:mm:ss:nnn format.</span></span> <span data-ttu-id="e138f-112">Vários arquivos de log com o mesmo valor de **TipoDeExibição** podem ser diferenciados usando o valor nesse e nos campos **LogStartTime** .</span><span class="sxs-lookup"><span data-stu-id="e138f-112">Multiple log files with the same **DisplayString** value can be differentiated by using the value in this and the **LogStartTime** fields.</span></span> <span data-ttu-id="e138f-113">Os valores nos campos **LogStartTime** e **LogStopTime** também permitem que o tempo total da coleção seja acessado rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e138f-113">The values in the **LogStartTime** and **LogStopTime** fields also allows the total collection time to be accessed quickly.</span></span>
-   <span data-ttu-id="e138f-114">**NumberOfRecords:** Número de amostras armazenadas na tabela para cada coleção de logs.</span><span class="sxs-lookup"><span data-stu-id="e138f-114">**NumberOfRecords:** Number of samples stored in the table for each log collection.</span></span>
-   <span data-ttu-id="e138f-115">**MinutesToUTC:** Valor usado para converter os dados de linha armazenados na hora UTC para a hora local.</span><span class="sxs-lookup"><span data-stu-id="e138f-115">**MinutesToUTC:** Value used to convert the row data stored in UTC time to local time.</span></span>
-   <span data-ttu-id="e138f-116">**TimeZoneName:** Nome do fuso horário em que os dados foram coletados.</span><span class="sxs-lookup"><span data-stu-id="e138f-116">**TimeZoneName:** Name of the time zone where the data was collected.</span></span> <span data-ttu-id="e138f-117">Se você estiver coletando ou tiver dados reconectados de um arquivo coletado em sistemas em seu próprio fuso horário, esse campo irá declarar o local.</span><span class="sxs-lookup"><span data-stu-id="e138f-117">If you are collecting or have relogged data from a file collected on systems in your own time zone, this field will state the location.</span></span>

<span data-ttu-id="e138f-118">**Observação**  Antes do Windows Vista, os conjuntos de coletores de dados eram armazenados no registro em</span><span class="sxs-lookup"><span data-stu-id="e138f-118">**Note**  Prior to Windows Vista, the data collector sets were stored in the registry at</span></span>

<span data-ttu-id="e138f-119">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ SysmonLog \\ logs queries**</span><span class="sxs-lookup"><span data-stu-id="e138f-119">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\SysmonLog\\Log Queries**</span></span>

<span data-ttu-id="e138f-120">.</span><span class="sxs-lookup"><span data-stu-id="e138f-120">.</span></span> <span data-ttu-id="e138f-121">Os campos listados acima não correspondem aos valores no registro.</span><span class="sxs-lookup"><span data-stu-id="e138f-121">The fields listed above do not correspond to the values in registry.</span></span> <span data-ttu-id="e138f-122">Para o Windows Vista, os conjuntos de coletores de dados não são armazenados no registro.</span><span class="sxs-lookup"><span data-stu-id="e138f-122">For Windows Vista, the data collector sets are not stored in the registry.</span></span>

 

 



