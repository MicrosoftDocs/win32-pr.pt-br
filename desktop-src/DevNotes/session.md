---
description: A estrutura de sessão contém informações sobre a sessão atual.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Estrutura de sessão
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646192"
---
# <a name="session-structure"></a><span data-ttu-id="809c1-103">Estrutura de sessão</span><span class="sxs-lookup"><span data-stu-id="809c1-103">SESSION structure</span></span>

<span data-ttu-id="809c1-104">\[Esta estrutura contém informações necessárias apenas ao usar as funções **DeleteExtractedFiles** e **Extract** , que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="809c1-104">\[This structure contains information required only when using the **DeleteExtractedFiles** and **Extract** functions, which are not supported.</span></span> <span data-ttu-id="809c1-105">Esta documentação é fornecida apenas para fins informativos.\]</span><span class="sxs-lookup"><span data-stu-id="809c1-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="809c1-106">A estrutura de **sessão** contém informações sobre a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="809c1-106">The **SESSION** structure contains information about the current session.</span></span>

## <a name="syntax"></a><span data-ttu-id="809c1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="809c1-107">Syntax</span></span>


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a><span data-ttu-id="809c1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="809c1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="809c1-109">**Act**</span><span class="sxs-lookup"><span data-stu-id="809c1-109">**act**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-110">a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="809c1-110">The action to perform.</span></span> <span data-ttu-id="809c1-111">Esse membro pode ser um dos valores do seguinte tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="809c1-111">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

<span data-ttu-id="809c1-112">**hflist**</span><span class="sxs-lookup"><span data-stu-id="809c1-112">**hflist**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-113">O identificador para uma lista de arquivos especificados na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="809c1-113">The handle to a list of files specified on the command line.</span></span> <span data-ttu-id="809c1-114">Esse tipo de dados é declarado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="809c1-114">This datatype is declared as follows:</span></span>

`typedef void *HFILELIST;`

</dd> <dt>

<span data-ttu-id="809c1-115">**fAllCabinets**</span><span class="sxs-lookup"><span data-stu-id="809c1-115">**fAllCabinets**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-116">Um sinalizador que indica se mais de um arquivo de gabinete deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="809c1-116">A flag that indicates whether more than one cabinet file should be processed.</span></span> <span data-ttu-id="809c1-117">Se esse valor for **true**, os gabinetes de continuação serão processados.</span><span class="sxs-lookup"><span data-stu-id="809c1-117">If this value is **TRUE**, continuation cabinets are processed.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-118">**fOverwrite**</span><span class="sxs-lookup"><span data-stu-id="809c1-118">**fOverwrite**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-119">Um sinalizador que indica se os arquivos existentes devem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="809c1-119">A flag that indicates whether existing files should be overwritten.</span></span> <span data-ttu-id="809c1-120">Se esse valor for **true**, os arquivos existentes serão substituídos.</span><span class="sxs-lookup"><span data-stu-id="809c1-120">If this value is **TRUE**, existing files are overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-121">**fNoLineFeed**</span><span class="sxs-lookup"><span data-stu-id="809c1-121">**fNoLineFeed**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-122">Um sinalizador que indica se a última `printf` chamada tem os caracteres de nova linha ( `\n` ).</span><span class="sxs-lookup"><span data-stu-id="809c1-122">A flag that indicates whether the last `printf` call has the newline (`\n`) characters.</span></span> <span data-ttu-id="809c1-123">Se esse valor for **true**, a última `printf` chamada não incluirá os caracteres de nova linha.</span><span class="sxs-lookup"><span data-stu-id="809c1-123">If this value is **TRUE**, the last `printf` call did not include the newline characters.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-124">**fSelfExtract**</span><span class="sxs-lookup"><span data-stu-id="809c1-124">**fSelfExtract**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-125">Um sinalizador que indica se um gabinete está auto-extraível.</span><span class="sxs-lookup"><span data-stu-id="809c1-125">A flag that indicates whether a cabinet is self extracting.</span></span> <span data-ttu-id="809c1-126">Se esse valor for **true**, o gabinete será auto-extraível.</span><span class="sxs-lookup"><span data-stu-id="809c1-126">If this value is **TRUE**, the cabinet is self extracting.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-127">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="809c1-127">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-128">O comprimento da parte executável (. exe) de um gabinete de extração automática.</span><span class="sxs-lookup"><span data-stu-id="809c1-128">The length of the executable (.exe) portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-129">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="809c1-129">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-130">O comprimento da parte do CAB de um gabinete de extração automática.</span><span class="sxs-lookup"><span data-stu-id="809c1-130">The length of the CAB portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-131">**ahfSelf**</span><span class="sxs-lookup"><span data-stu-id="809c1-131">**ahfSelf**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-132">Os identificadores de arquivo para o gabinete.</span><span class="sxs-lookup"><span data-stu-id="809c1-132">The file handles to the cabinet.</span></span>

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

<span data-ttu-id="809c1-133">**cErrors**</span><span class="sxs-lookup"><span data-stu-id="809c1-133">**cErrors**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-134">A contagem de erros encontrados durante a sessão de extração.</span><span class="sxs-lookup"><span data-stu-id="809c1-134">The count of errors encountered during the extraction session.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-135">**hfdi**</span><span class="sxs-lookup"><span data-stu-id="809c1-135">**hfdi**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-136">Um identificador para o contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="809c1-136">A handle to the FDI context.</span></span> <span data-ttu-id="809c1-137">Esse tipo de dados é declarado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="809c1-137">This datatype is declared as follows:</span></span>

`typedef void FAR *HFDI; `

</dd> <dt>

<span data-ttu-id="809c1-138">**erf**</span><span class="sxs-lookup"><span data-stu-id="809c1-138">**erf**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-139">A estrutura de erro FDI.</span><span class="sxs-lookup"><span data-stu-id="809c1-139">The FDI error structure.</span></span> <span data-ttu-id="809c1-140">Consulte [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span><span class="sxs-lookup"><span data-stu-id="809c1-140">See [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span></span>

</dd> <dt>

<span data-ttu-id="809c1-141">**recfiles**</span><span class="sxs-lookup"><span data-stu-id="809c1-141">**cFiles**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-142">A contagem de arquivos processados.</span><span class="sxs-lookup"><span data-stu-id="809c1-142">The count of files processed.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-143">**cbTotalBytes**</span><span class="sxs-lookup"><span data-stu-id="809c1-143">**cbTotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-144">O número total de bytes extraídos.</span><span class="sxs-lookup"><span data-stu-id="809c1-144">The total number of bytes extracted.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-145">**perr**</span><span class="sxs-lookup"><span data-stu-id="809c1-145">**perr**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-146">O FDI de passagem.</span><span class="sxs-lookup"><span data-stu-id="809c1-146">The pass through FDI.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-147">**Java**</span><span class="sxs-lookup"><span data-stu-id="809c1-147">**se**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-148">O erro do arquivo de despejo.</span><span class="sxs-lookup"><span data-stu-id="809c1-148">The spill file error.</span></span> <span data-ttu-id="809c1-149">Esse membro pode ser um dos valores do seguinte tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="809c1-149">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

<span data-ttu-id="809c1-150">**cbSpill**</span><span class="sxs-lookup"><span data-stu-id="809c1-150">**cbSpill**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-151">O tamanho do arquivo de despejo solicitado.</span><span class="sxs-lookup"><span data-stu-id="809c1-151">The size of the spill file requested.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-152">**achSelf**</span><span class="sxs-lookup"><span data-stu-id="809c1-152">**achSelf**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-153">O nome do arquivo executável (. exe).</span><span class="sxs-lookup"><span data-stu-id="809c1-153">The name of the executable (.exe) file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="809c1-154">**achMsg**</span><span class="sxs-lookup"><span data-stu-id="809c1-154">**achMsg**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-155">O buffer de formatação de mensagens.</span><span class="sxs-lookup"><span data-stu-id="809c1-155">The message formatting buffer.</span></span>

`#define cbMAX_LINE          256`

</dd> <dt>

<span data-ttu-id="809c1-156">**achLine**</span><span class="sxs-lookup"><span data-stu-id="809c1-156">**achLine**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-157">O buffer de formatação de linha.</span><span class="sxs-lookup"><span data-stu-id="809c1-157">The line formatting buffer.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-158">**achLocation**</span><span class="sxs-lookup"><span data-stu-id="809c1-158">**achLocation**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-159">O diretório de saída.</span><span class="sxs-lookup"><span data-stu-id="809c1-159">The output directory.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-160">**achFile**</span><span class="sxs-lookup"><span data-stu-id="809c1-160">**achFile**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-161">O nome de arquivo atual que está sendo extraído.</span><span class="sxs-lookup"><span data-stu-id="809c1-161">The current file name being extracted.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-162">**achDest**</span><span class="sxs-lookup"><span data-stu-id="809c1-162">**achDest**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-163">O nome do arquivo de destino forçado.</span><span class="sxs-lookup"><span data-stu-id="809c1-163">The forced destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-164">**achCabPath**</span><span class="sxs-lookup"><span data-stu-id="809c1-164">**achCabPath**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-165">O caminho para examinar um arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="809c1-165">The path to look at for a cabinet file.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-166">**fContinuationCabinet**</span><span class="sxs-lookup"><span data-stu-id="809c1-166">**fContinuationCabinet**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-167">Um sinalizador que indica se o gabinete atual é o primeiro processado.</span><span class="sxs-lookup"><span data-stu-id="809c1-167">A flag that indicates whether the current cabinet is the first one processed.</span></span> <span data-ttu-id="809c1-168">Se definido como **true**, ele não é o primeiro gabinete processado.</span><span class="sxs-lookup"><span data-stu-id="809c1-168">If set to **TRUE**, it is not the first cabinet processed.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-169">**fShowReserveInfo**</span><span class="sxs-lookup"><span data-stu-id="809c1-169">**fShowReserveInfo**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-170">Um sinalizador que indica se as informações de reserva devem ser fornecidas.</span><span class="sxs-lookup"><span data-stu-id="809c1-170">A flag that indicates whether reserve information should be provided.</span></span> <span data-ttu-id="809c1-171">Se definido como **true**, as informações serão disponibilizadas.</span><span class="sxs-lookup"><span data-stu-id="809c1-171">If set to **TRUE**, the information is made available.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-172">**fNextCabCalled**</span><span class="sxs-lookup"><span data-stu-id="809c1-172">**fNextCabCalled**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-173">Esse membro fornece uma maneira de determinar qual das entradas **acab** usar se estiver processando todos os arquivos em um conjunto de gabinetes (**fAllCabinet** é definido como **true**).</span><span class="sxs-lookup"><span data-stu-id="809c1-173">This member provides a way to determine which of the **acab** entries to use if we are processing all files in a cabinet set (**fAllCabinet** is set to **TRUE**).</span></span>

</dd> <dt>

<span data-ttu-id="809c1-174">**acab**</span><span class="sxs-lookup"><span data-stu-id="809c1-174">**acab**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-175">As duas últimas entradas no conjunto de gabinetes.</span><span class="sxs-lookup"><span data-stu-id="809c1-175">The last two entries in the cabinet set.</span></span> <span data-ttu-id="809c1-176">Essa estrutura é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="809c1-176">This structure is defined as follows:</span></span>

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

<span data-ttu-id="809c1-177">**achZap**</span><span class="sxs-lookup"><span data-stu-id="809c1-177">**achZap**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-178">O prefixo a ser tirado do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="809c1-178">The prefix to strip from the file name.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="809c1-179">**achCabinetFile**</span><span class="sxs-lookup"><span data-stu-id="809c1-179">**achCabinetFile**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-180">O arquivo de gabinete atual.</span><span class="sxs-lookup"><span data-stu-id="809c1-180">The current cabinet file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="809c1-181">**cArgv**</span><span class="sxs-lookup"><span data-stu-id="809c1-181">**cArgv**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-182">O argc de extração automática padrão.</span><span class="sxs-lookup"><span data-stu-id="809c1-182">The default self-extracting argc.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-183">**pArgv**</span><span class="sxs-lookup"><span data-stu-id="809c1-183">**pArgv**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-184">Um ponteiro para um ponteiro para o argv de extração automática padrão \[ \] .</span><span class="sxs-lookup"><span data-stu-id="809c1-184">A pointer to a pointer to the default self-extracting argv\[\].</span></span>

</dd> <dt>

<span data-ttu-id="809c1-185">**fDestructive**</span><span class="sxs-lookup"><span data-stu-id="809c1-185">**fDestructive**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-186">Um sinalizador que minimiza o espaço em disco necessário quando definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="809c1-186">A flag that minimizes the disk space needed when set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="809c1-187">**iCurrentFolder**</span><span class="sxs-lookup"><span data-stu-id="809c1-187">**iCurrentFolder**</span></span>
</dt> <dd>

<span data-ttu-id="809c1-188">Se **fDestructive** for definido como **true**, extraia apenas a pasta atual.</span><span class="sxs-lookup"><span data-stu-id="809c1-188">If **fDestructive** is set to **TRUE**, extract only the current folder.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="809c1-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="809c1-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809c1-190">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="809c1-190">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="809c1-191">**Extração**</span><span class="sxs-lookup"><span data-stu-id="809c1-191">**Extract**</span></span>](extract.md)
</dt> </dl>

 

 
