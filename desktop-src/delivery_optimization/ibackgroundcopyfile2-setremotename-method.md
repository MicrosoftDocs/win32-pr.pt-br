---
title: Método setremotename IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Altera o nome remoto para uma nova URL em um trabalho de download.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Método setremotename
- Método setremotename, interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, método setremotename
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455029"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a><span data-ttu-id="d7a84-106">Método IBackgroundCopyFile2:: setremotename</span><span class="sxs-lookup"><span data-stu-id="d7a84-106">IBackgroundCopyFile2::SetRemoteName method</span></span>

<span data-ttu-id="d7a84-107">Altera o nome remoto para uma nova URL em um trabalho de download.</span><span class="sxs-lookup"><span data-stu-id="d7a84-107">Changes the remote name to a new URL in a download job.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a84-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7a84-108">Syntax</span></span>


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a><span data-ttu-id="d7a84-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7a84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a84-110">*Remotoname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7a84-110">*RemoteName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7a84-111">Cadeia de caracteres terminada em nulo que contém o nome do arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="d7a84-111">Null-terminated string that contains the name of the file on the server.</span></span> <span data-ttu-id="d7a84-112">Para obter informações sobre como especificar o nome remoto, consulte o membro **RemoteName** .</span><span class="sxs-lookup"><span data-stu-id="d7a84-112">For information on specifying the remote name, see the **RemoteName** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a84-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7a84-113">Return value</span></span>

<span data-ttu-id="d7a84-114">Esse método retorna os seguintes valores de retorno, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="d7a84-114">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="d7a84-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d7a84-115">Return code</span></span>                                                                                  | <span data-ttu-id="d7a84-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7a84-116">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7a84-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="d7a84-118">Sucesso</span><span class="sxs-lookup"><span data-stu-id="d7a84-118">Success</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="d7a84-119"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-119"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d7a84-120">O novo nome remoto é uma URL inválida ou a nova URL é muito longa (a URL não pode exceder 2.200 caracteres).</span><span class="sxs-lookup"><span data-stu-id="d7a84-120">The new remote name is an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7a84-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7a84-121">Remarks</span></span>

<span data-ttu-id="d7a84-122">Normalmente, você chamará esse método se quiser alterar a URL usada para transferir o arquivo ou se quiser alterar o nome ou o caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d7a84-122">Typically, you call this method if you want to change the URL used to transfer the file or if you want to change the file name or path.</span></span>

<span data-ttu-id="d7a84-123">Esse método não serializa quando retorna.</span><span class="sxs-lookup"><span data-stu-id="d7a84-123">This method does not serialize when it returns.</span></span> <span data-ttu-id="d7a84-124">Para serializar a alteração, [**suspenda**](ibackgroundcopyjob-suspend.md) o trabalho, chame esse método (se estiver alterando vários arquivos no trabalho, use um loop) e [**retome**](ibackgroundcopyjob-resume.md) o trabalho.</span><span class="sxs-lookup"><span data-stu-id="d7a84-124">To serialize the change, [**suspend**](ibackgroundcopyjob-suspend.md) the job, call this method (if changing multiple files in the job, use a loop), and [**resume**](ibackgroundcopyjob-resume.md) the job.</span></span> <span data-ttu-id="d7a84-125">Chamar o método **método ibackgroundcopyjob:: resume** serializa a alteração.</span><span class="sxs-lookup"><span data-stu-id="d7a84-125">Calling the **IBackgroundCopyJob::Resume** method serializes the change.</span></span>

<span data-ttu-id="d7a84-126">Se o carimbo de data/hora ou o tamanho de arquivo do novo nome remoto for diferente do nome remoto anterior ou o novo servidor não der suporte à retomada do ponto de verificação (para nomes remotos HTTP), o reiniciará o download.</span><span class="sxs-lookup"><span data-stu-id="d7a84-126">If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), DO restarts the download.</span></span> <span data-ttu-id="d7a84-127">Caso contrário, a transferência será retomada da mesma posição no novo servidor.</span><span class="sxs-lookup"><span data-stu-id="d7a84-127">Otherwise, the transfer resumes from the same position on the new server.</span></span> <span data-ttu-id="d7a84-128">Não reinicia arquivos já transferidos.</span><span class="sxs-lookup"><span data-stu-id="d7a84-128">DO does not restart already transferred files.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a84-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a84-129">Requirements</span></span>



| <span data-ttu-id="d7a84-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a84-130">Requirement</span></span> | <span data-ttu-id="d7a84-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a84-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a84-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7a84-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a84-133">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="d7a84-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7a84-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7a84-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a84-135">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="d7a84-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d7a84-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7a84-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a84-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7a84-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="d7a84-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7a84-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d7a84-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7a84-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7a84-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d7a84-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d7a84-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7a84-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7a84-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d7a84-144">IID</span><span class="sxs-lookup"><span data-stu-id="d7a84-144">IID</span></span><br/>                      | <span data-ttu-id="d7a84-145">IID_IBackgroundCopyFile2 é definido como 83e81b93-0873-474D-8a8c-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="d7a84-145">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d7a84-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7a84-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a84-147">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="d7a84-147">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





