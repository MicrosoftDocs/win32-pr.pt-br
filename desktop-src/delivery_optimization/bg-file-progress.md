---
title: Estrutura de BG_FILE_PROGRESS (Deliveryoptimization. h)
description: A estrutura de BG_FILE_PROGRESS fornece informações de progresso relacionadas a arquivos, como o número de bytes transferidos.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Estrutura de BG_FILE_PROGRESS
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644991"
---
# <a name="bg_file_progress-structure"></a><span data-ttu-id="562d8-104">Estrutura de BG_FILE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="562d8-104">BG_FILE_PROGRESS structure</span></span>

<span data-ttu-id="562d8-105">A estrutura de **BG_FILE_PROGRESS** fornece informações de progresso relacionadas a arquivos, como o número de bytes transferidos.</span><span class="sxs-lookup"><span data-stu-id="562d8-105">The **BG_FILE_PROGRESS** structure provides file-related progress information, such as the number of bytes transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="562d8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="562d8-106">Syntax</span></span>


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="562d8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="562d8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="562d8-108">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="562d8-108">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="562d8-109">Tamanho do arquivo em bytes.</span><span class="sxs-lookup"><span data-stu-id="562d8-109">Size of the file in bytes.</span></span> <span data-ttu-id="562d8-110">Se o não puder determinar o tamanho do arquivo (por exemplo, se o arquivo ou o servidor não existir), o valor será DO_UNKNOWN_FILE_SIZE.</span><span class="sxs-lookup"><span data-stu-id="562d8-110">If DO cannot determine the size of the file (for example, if the file or server does not exist), the value is DO_UNKNOWN_FILE_SIZE.</span></span>

<span data-ttu-id="562d8-111">Se você estiver baixando intervalos de um arquivo, **bytesTotal** refletirá o número total de bytes que você deseja baixar do arquivo.</span><span class="sxs-lookup"><span data-stu-id="562d8-111">If you are downloading ranges from a file, **BytesTotal** reflects the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="562d8-112">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="562d8-112">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="562d8-113">Número de bytes transferidos.</span><span class="sxs-lookup"><span data-stu-id="562d8-113">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="562d8-114">**Concluído**</span><span class="sxs-lookup"><span data-stu-id="562d8-114">**Completed**</span></span>
</dt> <dd>

<span data-ttu-id="562d8-115">Para downloads, o valor será **true** se o arquivo estiver disponível para o usuário; caso contrário, o valor será **false**.</span><span class="sxs-lookup"><span data-stu-id="562d8-115">For downloads, the value is **TRUE** if the file is available to the user; otherwise, the value is **FALSE**.</span></span> <span data-ttu-id="562d8-116">Os arquivos estão disponíveis para o usuário depois de chamar o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="562d8-116">Files are available to the user after calling the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="562d8-117">Se o método **Complete** gerar um erro transitório, os arquivos processados antes do erro estarão disponíveis para o usuário; os outros não são.</span><span class="sxs-lookup"><span data-stu-id="562d8-117">If the **Complete** method generates a transient error, those files processed before the error occurred are available to the user; the others are not.</span></span> <span data-ttu-id="562d8-118">Use o membro **concluído** para determinar se o arquivo está disponível para o usuário quando a **conclusão** falhar.</span><span class="sxs-lookup"><span data-stu-id="562d8-118">Use the **Completed** member to determine if the file is available to the user when **Complete** fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="562d8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="562d8-119">Remarks</span></span>

<span data-ttu-id="562d8-120">Para determinar se o arquivo foi transferido, você pode:</span><span class="sxs-lookup"><span data-stu-id="562d8-120">To determine if DO transferred the file, you can:</span></span>

-   <span data-ttu-id="562d8-121">Compare **bytesTransferred** com **bytesTotal**.</span><span class="sxs-lookup"><span data-stu-id="562d8-121">Compare **BytesTransferred** to **BytesTotal**.</span></span>

## <a name="requirements"></a><span data-ttu-id="562d8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="562d8-122">Requirements</span></span>



| <span data-ttu-id="562d8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="562d8-123">Requirement</span></span> | <span data-ttu-id="562d8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="562d8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="562d8-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="562d8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="562d8-126">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="562d8-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="562d8-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="562d8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="562d8-128">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="562d8-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="562d8-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="562d8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="562d8-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="562d8-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562d8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="562d8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562d8-132">**BG_JOB_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="562d8-132">**BG_JOB_PROGRESS**</span></span>](bg-job-progress.md)
</dt> <dt>

[<span data-ttu-id="562d8-133">**IBackgroundCopyFile:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="562d8-133">**IBackgroundCopyFile::GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





