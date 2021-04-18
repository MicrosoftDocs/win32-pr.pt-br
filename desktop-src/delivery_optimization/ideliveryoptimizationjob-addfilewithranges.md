---
title: Método IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization. h)
description: Adiciona um arquivo a um trabalho de download e especifica os intervalos do arquivo que você deseja baixar.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Método AddFileWithRanges
- Método AddFileWithRanges, interface IDeliveryOptimizationJob
- Interface IDeliveryOptimizationJob, método AddFileWithRanges
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787637"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a><span data-ttu-id="7c364-106">Método IDeliveryOptimizationJob:: AddFileWithRanges</span><span class="sxs-lookup"><span data-stu-id="7c364-106">IDeliveryOptimizationJob::AddFileWithRanges method</span></span>

<span data-ttu-id="7c364-107">Adiciona um arquivo a um trabalho de download e especifica os intervalos do arquivo que você deseja baixar.</span><span class="sxs-lookup"><span data-stu-id="7c364-107">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c364-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c364-108">Syntax</span></span>


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a><span data-ttu-id="7c364-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c364-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c364-110">*FileID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c364-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c364-111">Cadeia de caracteres terminada em NULL que é um identificador exclusivo do conteúdo publicado.</span><span class="sxs-lookup"><span data-stu-id="7c364-111">Null terminated string that s an unique identifier of the published content.</span></span> <span data-ttu-id="7c364-112">Para conteúdo não publicado, pode ser qualquer cadeia de caracteres exclusiva que o chamador possa usar para identificar arquivos em um trabalho.</span><span class="sxs-lookup"><span data-stu-id="7c364-112">For non-published content, this can be any unique string that caller can use to identify files within a job.</span></span>

</dd> <dt>

<span data-ttu-id="7c364-113">*remoteUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c364-113">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c364-114">Cadeia de caracteres terminada em nulo que contém o nome do arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="7c364-114">Null-terminated string that contains the name of the file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="7c364-115">*LocalName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c364-115">*localName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c364-116">Cadeia de caracteres terminada em nulo que contém o nome do arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="7c364-116">Null-terminated string that contains the name of the file on the client.</span></span>

</dd> <dt>

<span data-ttu-id="7c364-117">*rangeCount* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7c364-117">*rangeCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c364-118">Número de elementos em *intervalos*.</span><span class="sxs-lookup"><span data-stu-id="7c364-118">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="7c364-119">*intervalos* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7c364-119">*ranges* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c364-120">Matriz de uma ou mais estruturas de [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) que especificam os intervalos a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="7c364-120">Array of one or more [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) structures that specify the ranges to download.</span></span> <span data-ttu-id="7c364-121">Não especifique intervalos duplicados ou sobrepostos.</span><span class="sxs-lookup"><span data-stu-id="7c364-121">Do not specify duplicate or overlapping ranges.</span></span>

</dd> <dt>

<span data-ttu-id="7c364-122">*tamanho* \[ de um em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7c364-122">*fileSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c364-123">Tamanho do arquivo em bytes.</span><span class="sxs-lookup"><span data-stu-id="7c364-123">Size of the file in bytes.</span></span> <span data-ttu-id="7c364-124">Passe **DO_UNKNOWN_FILE_SIZE** se o tamanho não for conhecido pelo aplicativo chamador.</span><span class="sxs-lookup"><span data-stu-id="7c364-124">Pass in **DO_UNKNOWN_FILE_SIZE** if size is not known to the caller application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c364-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c364-125">Return value</span></span>

<span data-ttu-id="7c364-126">Esse método retorna os seguintes valores de retorno, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="7c364-126">This method returns the following return values, as well as others.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7c364-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7c364-127">Return code</span></span></th>
<th><span data-ttu-id="7c364-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c364-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="7c364-129"><dt><strong><strong>S_OK</strong></strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7c364-129"><dt><strong><strong>S_OK</strong></strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7c364-130">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7c364-130">Success.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7c364-131"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7c364-131"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7c364-132">O nome do arquivo local é nulo ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="7c364-132">The local file name is NULL or empty string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="7c364-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7c364-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7c364-134">O usuário não tem permissão para gravar no diretório especificado no cliente.</span><span class="sxs-lookup"><span data-stu-id="7c364-134">User does not have permission to write to the specified directory on the client.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7c364-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7c364-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7c364-136">Um dos intervalos é inválido.</span><span class="sxs-lookup"><span data-stu-id="7c364-136">One of the ranges is invalid.</span></span> <span data-ttu-id="7c364-137">Por exemplo, InitialOffset é definido como <strong>BG_LENGTH_TO_EOF</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c364-137">For example, InitialOffset is set to <strong>BG_LENGTH_TO_EOF</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="7c364-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7c364-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7c364-139">Não é possível especificar intervalos duplicados ou sobrepostos.</span><span class="sxs-lookup"><span data-stu-id="7c364-139">You cannot specify duplicate or overlapping ranges.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7c364-140">Os intervalos são classificados pelo deslocamento do valor, não pelo comprimento.</span><span class="sxs-lookup"><span data-stu-id="7c364-140">The ranges are sorted by the offset of the value, not the length.</span></span> <span data-ttu-id="7c364-141">Se forem inseridos intervalos com o mesmo deslocamento, mas estiverem na ordem inversa, esse erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="7c364-141">If ranges are entered that have the same offset, but are in reverse order, then this error will be returned.</span></span> <span data-ttu-id="7c364-142">Por exemplo, se 100,5 e 100,0 forem inseridos nessa ordem, você não poderá adicionar o arquivo ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="7c364-142">For example, if 100.5 and 100.0 are entered in that order, then you will not be able to add the file to the job.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7c364-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7c364-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7c364-144">O estado do trabalho não pode ser <strong>BG_JOB_STATE_CANCELLED</strong> ou <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span><span class="sxs-lookup"><span data-stu-id="7c364-144">The state of the job cannot be <strong>BG_JOB_STATE_CANCELLED</strong> or <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="7c364-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c364-145">Requirements</span></span>



| <span data-ttu-id="7c364-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c364-146">Requirement</span></span> | <span data-ttu-id="7c364-147">Valor</span><span class="sxs-lookup"><span data-stu-id="7c364-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c364-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c364-148">Minimum supported client</span></span><br/> | <span data-ttu-id="7c364-149">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="7c364-149">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c364-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c364-150">Minimum supported server</span></span><br/> | <span data-ttu-id="7c364-151">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="7c364-151">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7c364-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c364-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c364-153"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c364-153"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c364-154">INSERI</span><span class="sxs-lookup"><span data-stu-id="7c364-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c364-155"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c364-155"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7c364-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c364-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c364-157"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c364-157"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7c364-158">DLL</span><span class="sxs-lookup"><span data-stu-id="7c364-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c364-159"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c364-159"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7c364-160">IID</span><span class="sxs-lookup"><span data-stu-id="7c364-160">IID</span></span><br/>                      | <span data-ttu-id="7c364-161">IID_IDeliveryOptimizationJob é definido como EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="7c364-161">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="7c364-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c364-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c364-163">**IDeliveryOptimizationJob**</span><span class="sxs-lookup"><span data-stu-id="7c364-163">**IDeliveryOptimizationJob**</span></span>](ideliveryoptimizationjob.md)
</dt> </dl>

 

