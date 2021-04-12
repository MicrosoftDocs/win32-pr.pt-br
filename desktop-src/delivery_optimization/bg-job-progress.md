---
title: Estrutura de BG_JOB_PROGRESS (Deliveryoptimization. h)
description: A estrutura de BG_JOB_PROGRESS fornece informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos. Para trabalhos de carregamento, o progresso se aplica ao arquivo de carregamento, não ao arquivo de resposta.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Estrutura de BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499631"
---
# <a name="bg_job_progress-structure"></a><span data-ttu-id="72312-105">Estrutura de BG_JOB_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="72312-105">BG_JOB_PROGRESS structure</span></span>

<span data-ttu-id="72312-106">A estrutura de **BG_JOB_PROGRESS** fornece informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos.</span><span class="sxs-lookup"><span data-stu-id="72312-106">The **BG_JOB_PROGRESS** structure provides job-related progress information, such as the number of bytes and files transferred.</span></span> <span data-ttu-id="72312-107">Para trabalhos de carregamento, o progresso se aplica ao arquivo de carregamento, não ao arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="72312-107">For upload jobs, the progress applies to the upload file, not the reply file.</span></span>

## <a name="syntax"></a><span data-ttu-id="72312-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72312-108">Syntax</span></span>


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="72312-109">Membros</span><span class="sxs-lookup"><span data-stu-id="72312-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="72312-110">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="72312-110">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="72312-111">Número total de bytes a serem transferidos para todos os arquivos no trabalho.</span><span class="sxs-lookup"><span data-stu-id="72312-111">Total number of bytes to transfer for all files in the job.</span></span> <span data-ttu-id="72312-112">Se o valor for BG_SIZE_UNKNOWN, o tamanho total de todos os arquivos no trabalho não será determinado.</span><span class="sxs-lookup"><span data-stu-id="72312-112">If the value is BG_SIZE_UNKNOWN, the total size of all files in the job has not been determined.</span></span> <span data-ttu-id="72312-113">Não definirá esse valor se ele não puder determinar o tamanho de um dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="72312-113">DO does not set this value if it cannot determine the size of one of the files.</span></span> <span data-ttu-id="72312-114">Por exemplo, se o arquivo ou servidor especificado não existir, o não poderá determinar o tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="72312-114">For example, if the specified file or server does not exist, DO cannot determine the size of the file.</span></span>

<span data-ttu-id="72312-115">Se você estiver baixando intervalos do arquivo, o **bytesTotal** incluirá o número total de bytes que você deseja baixar do arquivo.</span><span class="sxs-lookup"><span data-stu-id="72312-115">If you are downloading ranges from the file, **BytesTotal** includes the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="72312-116">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="72312-116">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="72312-117">Número de bytes transferidos.</span><span class="sxs-lookup"><span data-stu-id="72312-117">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="72312-118">**FilesTotal**</span><span class="sxs-lookup"><span data-stu-id="72312-118">**FilesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="72312-119">Número total de arquivos a serem transferidos para esse trabalho.</span><span class="sxs-lookup"><span data-stu-id="72312-119">Total number of files to transfer for this job.</span></span>

</dd> <dt>

<span data-ttu-id="72312-120">**FilesTransferred**</span><span class="sxs-lookup"><span data-stu-id="72312-120">**FilesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="72312-121">Número de arquivos transferidos.</span><span class="sxs-lookup"><span data-stu-id="72312-121">Number of files transferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72312-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72312-122">Requirements</span></span>



| <span data-ttu-id="72312-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="72312-123">Requirement</span></span> | <span data-ttu-id="72312-124">Valor</span><span class="sxs-lookup"><span data-stu-id="72312-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72312-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72312-125">Minimum supported client</span></span><br/> | <span data-ttu-id="72312-126">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="72312-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="72312-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72312-127">Minimum supported server</span></span><br/> | <span data-ttu-id="72312-128">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="72312-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="72312-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72312-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="72312-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="72312-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72312-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="72312-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72312-132">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="72312-132">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="72312-133">**Método ibackgroundcopyjob:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="72312-133">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





