---
title: Método IBackgroundCopyManager CreateJob (Deliveryoptimization.h)
description: Cria um trabalho.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Método CreateJob
- Método CreateJob, interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, método CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/27/2021
ms.locfileid: "104011881"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a><span data-ttu-id="9e9fe-106">Método IBackgroundCopyManager:: CreateJob</span><span class="sxs-lookup"><span data-stu-id="9e9fe-106">IBackgroundCopyManager::CreateJob method</span></span>

<span data-ttu-id="9e9fe-107">Cria um trabalho.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-107">Creates a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9fe-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e9fe-108">Syntax</span></span>


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="9e9fe-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e9fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e9fe-110">*pDisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e9fe-110">*pDisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9fe-111">Cadeia de caracteres terminada em nulo que contém um nome de exibição para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-111">Null-terminated string that contains a display name for the job.</span></span> <span data-ttu-id="9e9fe-112">Normalmente, o nome de exibição é usado para identificar o trabalho em uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-112">Typically, the display name is used to identify the job in a user interface.</span></span> <span data-ttu-id="9e9fe-113">Observe que mais de um trabalho pode ter o mesmo nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-113">Note that more than one job may have the same display name.</span></span> <span data-ttu-id="9e9fe-114">Não deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-114">Must not be **NULL**.</span></span> <span data-ttu-id="9e9fe-115">O nome é limitado a 256 caracteres, não incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-115">The name is limited to 256 characters, not including the null terminator.</span></span>

</dd> <dt>

<span data-ttu-id="9e9fe-116">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="9e9fe-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9fe-117">Tipo de trabalho de transferência, como BG_JOB_TYPE_DOWNLOAD.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-117">Type of transfer job, such as BG_JOB_TYPE_DOWNLOAD.</span></span> <span data-ttu-id="9e9fe-118">Para obter uma lista de tipos de transferência, consulte a enumeração [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="9e9fe-118">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="9e9fe-119">*pJobID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9e9fe-119">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9fe-120">Identifica exclusivamente seu trabalho na fila.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-120">Uniquely identifies your job in the queue.</span></span> <span data-ttu-id="9e9fe-121">Use esse identificador ao chamar o método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) para obter um trabalho da fila.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-121">Use this identifier when you call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method to get a job from the queue.</span></span>

</dd> <dt>

<span data-ttu-id="9e9fe-122">*ppJob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9e9fe-122">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9fe-123">Um ponteiro de interface [**método ibackgroundcopyjob**](ibackgroundcopyjob-.md) que você usa para modificar as propriedades do trabalho e especificar os arquivos a serem transferidos.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-123">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer that you use to modify the job's properties and specify the files to be transferred.</span></span> <span data-ttu-id="9e9fe-124">Para ativar o trabalho na fila, chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="9e9fe-124">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span> <span data-ttu-id="9e9fe-125">Libere *ppJob* quando terminar.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-125">Release *ppJob* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e9fe-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e9fe-126">Return value</span></span>

<span data-ttu-id="9e9fe-127">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-127">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="9e9fe-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9e9fe-128">Return code</span></span>                                                                              | <span data-ttu-id="9e9fe-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e9fe-129">Description</span></span>                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9e9fe-130"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9e9fe-130"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="9e9fe-131">Novo trabalho gerado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9e9fe-131">Successfully generated the new job.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e9fe-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e9fe-132">Remarks</span></span>

<span data-ttu-id="9e9fe-133">Somente o usuário que cria o trabalho ou um usuário com privilégios de administrador pode [Adicionar arquivos ao trabalho](https://www.bing.com/search?q=add+files+to+the+job) e [alterar as propriedades do trabalho](https://www.bing.com/search?q=change+the+job's+properties).</span><span class="sxs-lookup"><span data-stu-id="9e9fe-133">Only the user who creates the job or a user with administrator privileges can [add files to the job](https://www.bing.com/search?q=add+files+to+the+job) and [change the job's properties](https://www.bing.com/search?q=change+the+job's+properties).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e9fe-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e9fe-134">Requirements</span></span>



| <span data-ttu-id="9e9fe-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e9fe-135">Requirement</span></span> | <span data-ttu-id="9e9fe-136">Valor</span><span class="sxs-lookup"><span data-stu-id="9e9fe-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9fe-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e9fe-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9e9fe-138">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="9e9fe-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9e9fe-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e9fe-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9e9fe-140">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="9e9fe-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9e9fe-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e9fe-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e9fe-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e9fe-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e9fe-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="9e9fe-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e9fe-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e9fe-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9e9fe-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e9fe-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e9fe-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e9fe-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9e9fe-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9e9fe-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e9fe-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e9fe-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9e9fe-149">IID</span><span class="sxs-lookup"><span data-stu-id="9e9fe-149">IID</span></span><br/>                      | <span data-ttu-id="9e9fe-150">IID_IBackgroundCopyManager é definido como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="9e9fe-150">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9e9fe-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e9fe-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9fe-152">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="9e9fe-152">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="9e9fe-153">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="9e9fe-153">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="9e9fe-154">**Método ibackgroundcopyjob:: retomar**</span><span class="sxs-lookup"><span data-stu-id="9e9fe-154">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>
