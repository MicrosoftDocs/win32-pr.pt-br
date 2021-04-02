---
description: Os gravadores podem ajustar o desempenho de vários tipos de backup no nível de conjunto de arquivos, indicando por meio de um tipo de backup de especificação de arquivo, indicado por uma máscara de bits ou uma operação de bit ou de membros da \_ enumeração do tipo de backup spec do arquivo VSS \_ \_ \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Suporte a esquema de nível de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922716"
---
# <a name="file-level-schema-support"></a><span data-ttu-id="a8567-103">Suporte a esquema de nível de arquivo</span><span class="sxs-lookup"><span data-stu-id="a8567-103">File Level Schema Support</span></span>

<span data-ttu-id="a8567-104">Os gravadores podem ajustar o desempenho de vários tipos de backup no nível de [*conjunto de arquivos*](vssgloss-f.md) , indicando por meio de um tipo de backup de especificação de arquivo, indicado por uma máscara de bits ou uma operação de bit ou de membros da enumeração do [**\_ \_ \_ \_ tipo de backup spec do arquivo VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) .</span><span class="sxs-lookup"><span data-stu-id="a8567-104">Writers can fine-tune the performance of various types of backup at the [*file set*](vssgloss-f.md) level by indicating through a file specification backup type, indicated by a bit mask or bitwise OR of the members of the [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) enumeration.</span></span>

<span data-ttu-id="a8567-105">Para tipos de backup especificados, o gravador indica o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a8567-105">For specified types of backup, the writer indicates the following:</span></span>

-   <span data-ttu-id="a8567-106">Se será necessário fazer cópias de sombra do volume para fazer backup de um conjunto de arquivos corretamente.</span><span class="sxs-lookup"><span data-stu-id="a8567-106">Whether it will be necessary to shadow copy the volume to properly back up a file set.</span></span> <span data-ttu-id="a8567-107">Por exemplo, se os arquivos em um conjunto de arquivos não forem abertos exclusivamente pelo gravador e ele puder garantir que seja estável, uma cópia de sombra não será necessária.</span><span class="sxs-lookup"><span data-stu-id="a8567-107">For instance, if the files in a file set are not exclusively opened by the writer and it can ensure that it is stable, a shadow copy is not needed.</span></span>
-   <span data-ttu-id="a8567-108">Se o solicitante precisa executar o backup de forma que, independentemente da hora da última modificação ou de outros problemas, a versão dos arquivos do conjunto de arquivo atual no backup será restaurada.</span><span class="sxs-lookup"><span data-stu-id="a8567-108">Whether the requester has to perform the backup in such a way that, regardless of last modification time or other issues, the version of the file set's files current at backup will be restored.</span></span> <span data-ttu-id="a8567-109">Normalmente, isso significa que o conjunto de arquivos é copiado como parte do backup.</span><span class="sxs-lookup"><span data-stu-id="a8567-109">Typically, this means that the file set is copied as part of the backup.</span></span>

<span data-ttu-id="a8567-110">Os valores do [**\_ tipo de \_ \_ backup \_ de especificação do arquivo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indicam o requisito de cópia de sombra são:</span><span class="sxs-lookup"><span data-stu-id="a8567-110">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate shadow copy requirement are:</span></span>

-   <span data-ttu-id="a8567-111">\_FSBT VSS \_ todos os \_ instantâneos \_ necessários</span><span class="sxs-lookup"><span data-stu-id="a8567-111">VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="a8567-112">\_instantâneo completo do VSS FSBT \_ \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-112">VSS\_FSBT\_FULL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="a8567-113">\_ \_ instantâneo diferencial do VSS FSBT \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-113">VSS\_FSBT\_DIFFERENTIAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="a8567-114">\_instantâneo incremental do VSS FSBT \_ \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-114">VSS\_FSBT\_INCREMENTAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="a8567-115">instantâneo de log de FSBT do VSS \_ \_ \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-115">VSS\_FSBT\_LOG\_SNAPSHOT\_REQUIRED</span></span>

<span data-ttu-id="a8567-116">Os valores do [**\_ tipo de \_ \_ backup \_ de especificação do arquivo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indicam a necessidade de fazer backup de um arquivo são:</span><span class="sxs-lookup"><span data-stu-id="a8567-116">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate the requirement to back up a file are:</span></span>

-   <span data-ttu-id="a8567-117">BACKUP do VSS \_ FSBT \_ todo \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-117">VSS\_FSBT\_ALL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="a8567-118">\_backup completo do VSS FSBT \_ \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-118">VSS\_FSBT\_FULL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="a8567-119">\_ \_ backup diferencial do VSS FSBT \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-119">VSS\_FSBT\_DIFFERENTIAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="a8567-120">\_backup incremental do VSS FSBT \_ \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-120">VSS\_FSBT\_INCREMENTAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="a8567-121">\_backup de log FSBT do VSS \_ \_ \_ necessário</span><span class="sxs-lookup"><span data-stu-id="a8567-121">VSS\_FSBT\_LOG\_BACKUP\_REQUIRED</span></span>

<span data-ttu-id="a8567-122">Por padrão, os conjuntos de arquivos são marcados com um tipo de backup de especificação de arquivo de VSS \_ FSBT \_ todos os \_ backups \_ necessários \| VSS \_ FSBT \_ todo o \_ instantâneo \_ necessário, o que significa que uma cópia de sombra é sempre necessária para lidar com os arquivos do conjunto de arquivos e que os arquivos devem ser copiados em todos os tipos de backup.</span><span class="sxs-lookup"><span data-stu-id="a8567-122">By default, file sets are tagged with a file specification backup type of VSS\_FSBT\_ALL\_BACKUP\_REQUIRED \| VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED, meaning that a shadow copy is always required in handling the file set's files, and that the files should be copied in all types of backup.</span></span>

 

 



