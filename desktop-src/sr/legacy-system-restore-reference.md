---
title: Referência de restauração do sistema herdada
description: Esta documentação descreve os detalhes de implementação do repositório usado por uma versão herdada da restauração do sistema. Ele não se aplica à implementação da restauração do sistema no Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822289"
---
# <a name="legacy-system-restore-reference"></a><span data-ttu-id="74edc-104">Referência de restauração do sistema herdada</span><span class="sxs-lookup"><span data-stu-id="74edc-104">Legacy System Restore Reference</span></span>

<span data-ttu-id="74edc-105">\[Essas informações se aplicam somente ao Windows XP com Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="74edc-105">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="74edc-106">Esta documentação descreve os detalhes de implementação do repositório usado por uma versão herdada da restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="74edc-106">This documentation describes implementation details of the repository used by a legacy version of System Restore.</span></span> <span data-ttu-id="74edc-107">Ele não se aplica à implementação da restauração do sistema no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="74edc-107">It does not apply to the implementation of System Restore on Windows Vista.</span></span>

## <a name="system-restore-repository-structure"></a><span data-ttu-id="74edc-108">Estrutura do repositório de restauração do sistema</span><span class="sxs-lookup"><span data-stu-id="74edc-108">System Restore Repository Structure</span></span>

<span data-ttu-id="74edc-109">O Windows XP com SP2 contém um repositório para a restauração do sistema na seguinte pasta:% SYSTEMDRIVE% \\ informações de volume do sistema.</span><span class="sxs-lookup"><span data-stu-id="74edc-109">Windows XP with SP2 contains a repository for System Restore in the following folder: %SYSTEMDRIVE%\\System Volume Information.</span></span> <span data-ttu-id="74edc-110">Esse repositório contém informações para pontos de restauração, que são essencialmente um instantâneo do sistema em um momento no tempo.</span><span class="sxs-lookup"><span data-stu-id="74edc-110">This repository contains information for restore points, which are essentially a snapshot of the system at a moment in time.</span></span>

<span data-ttu-id="74edc-111">O repositório é estruturado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="74edc-111">The repository is structured as follows:</span></span>

<span data-ttu-id="74edc-112">Restauração de **informações de volume do sistema**    \*\* \_ {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **RP \* n** \*     \*\* \_ Restore {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **RP \* n**\*</span><span class="sxs-lookup"><span data-stu-id="74edc-112">**System Volume Information**    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*</span></span>

<span data-ttu-id="74edc-113">Para determinar qual \_ pasta de restauração {*GUID*} usar, leia o **GUID** especificado no seguinte arquivo: SYSTEMROOT% \\ System32 \\ Restore \\MachineGUID.txt.</span><span class="sxs-lookup"><span data-stu-id="74edc-113">To determine which \_restore{*GUID*} folder to use, read the **GUID** specified in the following file: SYSTEMROOT%\\System32\\Restore\\MachineGUID.txt.</span></span>

<span data-ttu-id="74edc-114">Dentro de cada \_ pasta Restore {*GUID*}, o \_ arquivo Driver. cfg contém informações de uma estrutura de **configuração do Sr \_ persistent \_** definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="74edc-114">Within each \_restore{*GUID*} folder, the \_driver.cfg file contains information from a **SR\_PERSISTENT\_CONFIG** structure defined as follows:</span></span>

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a><span data-ttu-id="74edc-115">Arquivos contidos em cada pasta RP *n*</span><span class="sxs-lookup"><span data-stu-id="74edc-115">Files Contained in Each RP *n* Folder</span></span>

<span data-ttu-id="74edc-116">Cada pasta RP *n* contém uma pasta de instantâneo que contém o seguinte:</span><span class="sxs-lookup"><span data-stu-id="74edc-116">Each RP *n* folder contains a Snapshot folder that contains the following:</span></span>

-   <span data-ttu-id="74edc-117">Um instantâneo dos hives do registro</span><span class="sxs-lookup"><span data-stu-id="74edc-117">A snapshot of the registry hives</span></span>
-   <span data-ttu-id="74edc-118">Uma pasta de repositório que contém um instantâneo do repositório WMI</span><span class="sxs-lookup"><span data-stu-id="74edc-118">A Repository folder that contains a snapshot of the WMI repository</span></span>
-   <span data-ttu-id="74edc-119">Um instantâneo do banco de dados COM+</span><span class="sxs-lookup"><span data-stu-id="74edc-119">A snapshot of the COM+ database</span></span>
-   <span data-ttu-id="74edc-120">Um instantâneo do banco de dados do IIS</span><span class="sxs-lookup"><span data-stu-id="74edc-120">A snapshot of the IIS database</span></span>

<span data-ttu-id="74edc-121">Cada pasta RP *n* contém um arquivo RP. log que contém informações gerais sobre o ponto de restauração da estrutura [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .</span><span class="sxs-lookup"><span data-stu-id="74edc-121">Each RP *n* folder contains an RP.log file that contains general information about the restore point from the [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) structure.</span></span>

<span data-ttu-id="74edc-122">Cada pasta RP *n* pode conter arquivos usados para controlar as alterações de um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="74edc-122">Each RP *n* folder may contain files used to track changes for a restore point.</span></span> <span data-ttu-id="74edc-123">O primeiro arquivo é chamado Change. log, o próximo arquivo é chamado Change. log. 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="74edc-123">The first file is named change.log, the next file is named change.log.1, and so on.</span></span> <span data-ttu-id="74edc-124">Cada arquivo de log de alterações contém as seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="74edc-124">Each change log file contains the following structures:</span></span>

-   [<span data-ttu-id="74edc-125">**ALTERAR \_ cabeçalho do log \_**</span><span class="sxs-lookup"><span data-stu-id="74edc-125">**CHANGE\_LOG\_HEADER**</span></span>](change-log-header.md)
-   <span data-ttu-id="74edc-126">[**Alterar \_ \_Entrada de log**](change-log-entry.md)1</span><span class="sxs-lookup"><span data-stu-id="74edc-126">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)1</span></span>
-   <span data-ttu-id="74edc-127">[**Alterar \_ \_Entrada de log**](change-log-entry.md)2</span><span class="sxs-lookup"><span data-stu-id="74edc-127">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)2</span></span>
-   <span data-ttu-id="74edc-128">...</span><span class="sxs-lookup"><span data-stu-id="74edc-128">...</span></span>
-   <span data-ttu-id="74edc-129">[**Alterar \_ \_Entrada de log**](change-log-entry.md)*n*</span><span class="sxs-lookup"><span data-stu-id="74edc-129">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)*n*</span></span>

## <a name="related-topics"></a><span data-ttu-id="74edc-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74edc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74edc-131">Estruturas de restauração do sistema herdadas</span><span class="sxs-lookup"><span data-stu-id="74edc-131">Legacy System Restore Structures</span></span>](legacy-system-restore-structures.md)
</dt> </dl>

 

 




