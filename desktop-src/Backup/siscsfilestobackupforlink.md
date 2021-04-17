---
title: Função SisCSFilesToBackupForLink (Sisbkup. h)
description: Retorna informações que descrevem os arquivos de armazenamento comuns aos quais o link do SIS especificado aponta.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Backup de função SisCSFilesToBackupForLink
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755462"
---
# <a name="siscsfilestobackupforlink-function"></a><span data-ttu-id="420f4-104">Função SisCSFilesToBackupForLink</span><span class="sxs-lookup"><span data-stu-id="420f4-104">SisCSFilesToBackupForLink function</span></span>

<span data-ttu-id="420f4-105">A função **SisCSFilesToBackupForLink** retorna informações que descrevem os arquivos de armazenamento comuns aos quais o link do SIS especificado aponta.</span><span class="sxs-lookup"><span data-stu-id="420f4-105">The **SisCSFilesToBackupForLink** function returns information describing the common-store files the specified SIS link points to.</span></span>

## <a name="syntax"></a><span data-ttu-id="420f4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="420f4-106">Syntax</span></span>


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="420f4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="420f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="420f4-108">*sisBackupStructure* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="420f4-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420f4-109">Ponteiro para a estrutura de backup do SIS retornada de [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="420f4-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="420f4-110">*reparseData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="420f4-110">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420f4-111">Ponteiro para o conteúdo do ponto de nova análise do SIS.</span><span class="sxs-lookup"><span data-stu-id="420f4-111">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="420f4-112">Esse ponto de nova análise contém dados que descrevem um link do SIS.</span><span class="sxs-lookup"><span data-stu-id="420f4-112">This reparse point contains data describing a SIS link.</span></span> <span data-ttu-id="420f4-113">Para recuperar os dados do ponto de nova análise de um arquivo, use o código de controle [**fsctl \_ Get de \_ \_ ponto de nova análise**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .</span><span class="sxs-lookup"><span data-stu-id="420f4-113">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="420f4-114">*reparseDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="420f4-114">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420f4-115">Tamanho do conteúdo do ponto de nova análise do SIS apontado por *reparseData*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="420f4-115">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="420f4-116">*thisFileContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="420f4-116">*thisFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="420f4-117">Ponteiro para uma cadeia de caracteres de contexto fornecida pelo aplicativo de backup que chama essa função.</span><span class="sxs-lookup"><span data-stu-id="420f4-117">Pointer to a context string supplied by the backup application calling this function.</span></span> <span data-ttu-id="420f4-118">O conteúdo dessa cadeia de caracteres de conteúdo é totalmente determinado por esse aplicativo de backup e não é interpretado pela API de backup do SIS.</span><span class="sxs-lookup"><span data-stu-id="420f4-118">The contents of this content string are entirely determined by this backup application and is not interpreted by the SIS Backup API.</span></span> <span data-ttu-id="420f4-119">Esse parâmetro é opcional; Se não for usado, defina o valor desse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="420f4-119">This parameter is optional; if not used, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="420f4-120">O valor desse parâmetro não será processado nesse caso.</span><span class="sxs-lookup"><span data-stu-id="420f4-120">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="420f4-121">*matchingFileContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="420f4-121">*matchingFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="420f4-122">Ponteiro de indireto duplo para a cadeia de caracteres de contexto do link do SIS identificado pelas informações passadas nos quatro primeiros parâmetros dessa função.</span><span class="sxs-lookup"><span data-stu-id="420f4-122">Doubly-indirect pointer to the context string of the SIS link identified by the information passed in the first four parameters of this function.</span></span> <span data-ttu-id="420f4-123">Esse parâmetro é opcional; se uma cadeia de caracteres de contexto não for fornecida como o valor do parâmetro *thisFileContext* , defina o valor desse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="420f4-123">This parameter is optional; if a context string is not provided as the value of the *thisFileContext* parameter, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="420f4-124">O valor desse parâmetro não será processado nesse caso.</span><span class="sxs-lookup"><span data-stu-id="420f4-124">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="420f4-125">*countOfCommonStoreFilesToBackUp* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="420f4-125">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="420f4-126">Número de arquivos listados no parâmetro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="420f4-126">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="420f4-127">*commonStoreFilesToBackUp* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="420f4-127">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="420f4-128">Ponteiro para uma matriz de nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="420f4-128">Pointer to an array of file names.</span></span> <span data-ttu-id="420f4-129">Esses arquivos devem ser armazenados em backup ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comuns solicitados pelo [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="420f4-129">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="420f4-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="420f4-130">Return value</span></span>

<span data-ttu-id="420f4-131">Essa função retornará **true** se for concluída com êxito e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="420f4-131">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="420f4-132">Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="420f4-132">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="420f4-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="420f4-133">Remarks</span></span>

<span data-ttu-id="420f4-134">O aplicativo de backup deve chamar essa função apenas uma vez para cada arquivo de link do SIS cujo backup está sendo feito.</span><span class="sxs-lookup"><span data-stu-id="420f4-134">The backup application should call this function only once for each SIS link file being backed up.</span></span>

<span data-ttu-id="420f4-135">O aplicativo de backup pode identificar um ponto de nova análise do SIS por sua marca, a marca de nova análise de e/s \_ \_ \_ SIS.</span><span class="sxs-lookup"><span data-stu-id="420f4-135">The backup application can identify a SIS reparse point by its tag, IO\_REPARSE\_TAG\_SIS.</span></span> <span data-ttu-id="420f4-136">Essa marca é definida em Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="420f4-136">This tag is defined in Winnt.h.</span></span>

<span data-ttu-id="420f4-137">Se esse ponto de nova análise identificado pelo valor do parâmetro *reparseData* descrever a primeira instância de um arquivo a ser armazenado em backup, essa função retornará **NULL** como o valor do parâmetro *matchingFileContext* e inicializará o valor da matriz *commonStoreFilesToBackUp* de cadeias de caracteres com os nomes do arquivo de armazenamento comum ou dos arquivos cujo backup será feito.</span><span class="sxs-lookup"><span data-stu-id="420f4-137">If this reparse point identified by the value of the *reparseData* parameter describes the first instance of a file to be backed up, this function will return **NULL** as the value of the *matchingFileContext* parameter, and initialize the value of the *commonStoreFilesToBackUp* array of strings with the names of the common-store file or files to be backed up.</span></span> <span data-ttu-id="420f4-138">Caso contrário, essa função definirá o valor do parâmetro *matchingFileContext* como a cadeia de caracteres de contexto correspondente à primeira instância do arquivo especificado e definirá o valor do parâmetro *countOfCommonStoreFilesToBackUp* como 0.</span><span class="sxs-lookup"><span data-stu-id="420f4-138">Otherwise, this function will set the value of the *matchingFileContext* parameter to the context string corresponding to the first instance of the specified file and set the value of the *countOfCommonStoreFilesToBackUp* parameter to 0.</span></span> <span data-ttu-id="420f4-139">Se houver vários arquivos de repositório comum correspondentes ao link especificado, o valor do parâmetro *thisFileContext* será a cadeia de caracteres de contexto correspondente ao primeiro arquivo de repositório comum retornado na matriz, que é, commonStoreFilesToBackUp \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="420f4-139">If there are multiple common-store files corresponding to the specified link, the value of the *thisFileContext* parameter will be the context string corresponding to the first common-store file returned in the array that is, commonStoreFilesToBackUp\[0\].</span></span>

<span data-ttu-id="420f4-140">A versão atual dessa função retornará no máximo um arquivo de armazenamento comum, mas é possível que, em versões futuras, um único link possa ser apoiado por vários arquivos de armazenamento comum, por exemplo, um para cada fluxo no arquivo, de modo que o aplicativo de backup deve dar suporte a vários arquivos em cada chamada para essa função.</span><span class="sxs-lookup"><span data-stu-id="420f4-140">The current version of this function will return at most one common-store file, but it is possible that in future versions a single link may be backed by several common-store files for example, one for each stream in the file so your backup application should support multiple files in each call to this function.</span></span> <span data-ttu-id="420f4-141">Em qualquer caso, cada arquivo de repositório comum será retornado no máximo uma vez para cada passagem de backup.</span><span class="sxs-lookup"><span data-stu-id="420f4-141">In any case, each common-store file will be returned at most once for each backup pass.</span></span>

<span data-ttu-id="420f4-142">O aplicativo de backup deve fazer backup ou restaurar o arquivo de repositório comum ou os arquivos identificados pelo nome do arquivo ou pelos nomes de arquivo retornados no parâmetro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="420f4-142">Your backup application should back up or restore the common-store file or files identified by the file name or file names returned in the *commonStoreFilesToBackUp* parameter.</span></span> <span data-ttu-id="420f4-143">Independentemente de haver um arquivo de repositório comum correspondente, o aplicativo de backup deve fazer backup do arquivo de link do SIS como ele existe no disco, por exemplo, como um ponto de nova análise e um arquivo esparso, e provavelmente sem intervalos preenchidos.</span><span class="sxs-lookup"><span data-stu-id="420f4-143">Regardless of whether there is a corresponding common-store file, your backup application should back up the SIS link file as it exists on the disk for example, as a reparse point and a sparse file, and most likely with no ranges filled in.</span></span> <span data-ttu-id="420f4-144">Seu aplicativo de backup pode fazer backup ou restaurar o arquivo de armazenamento comum ou os arquivos imediatamente, adiar o backup deles ou combiná-los conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="420f4-144">Your backup application may back up or restore the common-store file or files immediately, postpone backing them up, or mix them together as necessary.</span></span>

<span data-ttu-id="420f4-145">Depois que a operação de backup for concluída, Desaloque a memória usada pela matriz *commonStoreFilesToBackUp* de cadeias de caracteres chamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="420f4-145">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="420f4-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="420f4-146">Requirements</span></span>



| <span data-ttu-id="420f4-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="420f4-147">Requirement</span></span> | <span data-ttu-id="420f4-148">Valor</span><span class="sxs-lookup"><span data-stu-id="420f4-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="420f4-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="420f4-149">Minimum supported client</span></span><br/> | <span data-ttu-id="420f4-150">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="420f4-150">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="420f4-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="420f4-151">Minimum supported server</span></span><br/> | <span data-ttu-id="420f4-152">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="420f4-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="420f4-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="420f4-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="420f4-154"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="420f4-154"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="420f4-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="420f4-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="420f4-156"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="420f4-156"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="420f4-157">DLL</span><span class="sxs-lookup"><span data-stu-id="420f4-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="420f4-158"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="420f4-158"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="420f4-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="420f4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="420f4-160">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="420f4-160">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="420f4-161">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="420f4-161">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

