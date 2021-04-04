---
title: Função SisRestoredLink (Sisbkup. h)
description: Retorna os nomes do arquivo de repositório comum ou dos arquivos apontados pelo link SIS restaurado especificado.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Backup de função SisRestoredLink
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918176"
---
# <a name="sisrestoredlink-function"></a><span data-ttu-id="378ef-104">Função SisRestoredLink</span><span class="sxs-lookup"><span data-stu-id="378ef-104">SisRestoredLink function</span></span>

<span data-ttu-id="378ef-105">A função **SisRestoredLink** retorna os nomes do arquivo de repositório comum ou arquivos apontados pelo link SIS restaurado especificado.</span><span class="sxs-lookup"><span data-stu-id="378ef-105">The **SisRestoredLink** function returns the names of the common-store file or files pointed to by the specified restored SIS link.</span></span>

## <a name="syntax"></a><span data-ttu-id="378ef-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="378ef-106">Syntax</span></span>


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="378ef-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="378ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="378ef-108">*sisRestoreStructure* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378ef-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ef-109">Ponteiro para uma estrutura de restauração do SIS retornada de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="378ef-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="378ef-110">*restoredFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378ef-110">*restoredFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ef-111">Nome de arquivo totalmente qualificado do arquivo de link do SIS restaurado.</span><span class="sxs-lookup"><span data-stu-id="378ef-111">Fully qualified file name of the restored SIS link file.</span></span>

</dd> <dt>

<span data-ttu-id="378ef-112">*reparseData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378ef-112">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ef-113">Ponteiro para o conteúdo do ponto de nova análise do SIS.</span><span class="sxs-lookup"><span data-stu-id="378ef-113">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="378ef-114">Esse ponto de nova análise contém dados que descrevem o link do SIS restaurado.</span><span class="sxs-lookup"><span data-stu-id="378ef-114">This reparse point contains data describing the restored SIS link.</span></span> <span data-ttu-id="378ef-115">Para recuperar os dados do ponto de nova análise de um arquivo, use o código de controle [**fsctl \_ Get de \_ \_ ponto de nova análise**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .</span><span class="sxs-lookup"><span data-stu-id="378ef-115">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="378ef-116">*reparseDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378ef-116">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ef-117">Tamanho do conteúdo do ponto de nova análise do SIS apontado por *reparseData*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="378ef-117">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="378ef-118">*countOfCommonStoreFilesToRestore* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="378ef-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="378ef-119">Número de arquivos listados no parâmetro *commonStoreFilesToRestore* .</span><span class="sxs-lookup"><span data-stu-id="378ef-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="378ef-120">*commonStoreFilesToRestore* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="378ef-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="378ef-121">Ponteiro para uma matriz de nomes de arquivos de repositório comum.</span><span class="sxs-lookup"><span data-stu-id="378ef-121">Pointer to an array of common-store file names.</span></span> <span data-ttu-id="378ef-122">Esses arquivos devem ser restaurados ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comuns solicitados pelo [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="378ef-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

<span data-ttu-id="378ef-123">Se o valor do parâmetro *countOfCommonStoreFilesToRestore* não for 0, o valor do parâmetro *commonStoreFilesToRestore* conterá os nomes dos arquivos de armazenamento comuns a serem restaurados como resultado da restauração do link do SIS.</span><span class="sxs-lookup"><span data-stu-id="378ef-123">If the value of the *countOfCommonStoreFilesToRestore* parameter is not 0, the value of the *commonStoreFilesToRestore* parameter will contain the names of the common-store files to be restored as a result of restoring the SIS link.</span></span> <span data-ttu-id="378ef-124">Se o valor for 0, os arquivos de armazenamento comum foram retornados uma vez ou já estão presentes no volume.</span><span class="sxs-lookup"><span data-stu-id="378ef-124">If the value is 0, then either the common-store files have been returned once, or they are already present on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="378ef-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="378ef-125">Return value</span></span>

<span data-ttu-id="378ef-126">Essa função retornará **true** se for concluída com êxito e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="378ef-126">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="378ef-127">Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="378ef-127">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="378ef-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="378ef-128">Remarks</span></span>

<span data-ttu-id="378ef-129">Você deve chamar essa função para cada link do SIS que foi restaurado.</span><span class="sxs-lookup"><span data-stu-id="378ef-129">You should call this function for each SIS link that has been restored.</span></span>

<span data-ttu-id="378ef-130">Esta função retornará cada arquivo de repositório comum no máximo uma vez para cada operação de restauração; qualquer tentativa de restaurar links adicionais do SIS que veem o mesmo arquivo de armazenamento comum não resultará no retorno do nome do arquivo de repositório comum.</span><span class="sxs-lookup"><span data-stu-id="378ef-130">This function will return each common-store file at most once for each restore operation; any attempt to restore additional SIS links that see the same common-store file will not result in that common-store file name being returned.</span></span>

<span data-ttu-id="378ef-131">Essa função não retornará um arquivo de repositório comum que também não foi retornado em uma chamada para [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) durante a operação de backup, supondo que os dados de nova análise do SIS armazenados na mídia não tenham sido corrompidos.</span><span class="sxs-lookup"><span data-stu-id="378ef-131">This function will not return a common-store file that was not also returned in a call to [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) during the backup operation, assuming that the SIS reparse data stored on the media has not been corrupted.</span></span>

<span data-ttu-id="378ef-132">Ao restaurar um link do SIS, a operação de restauração deve criar apenas o arquivo esparso apropriado, inicializar os intervalos alocados e, em seguida, gravar os dados de nova análise do SIS exatamente como eles foram lidos durante a operação de backup.</span><span class="sxs-lookup"><span data-stu-id="378ef-132">When restoring a SIS link, your restore operation should create only the appropriate sparse file, initialize any allocated ranges, and then write the SIS reparse data exactly as it was read during the backup operation.</span></span> <span data-ttu-id="378ef-133">É crucial que a operação de restauração Crie arquivos esparsos com intervalos não alocados em vez de arquivos esparsos (ou arquivos não SPARSE) inicializados com zeros.</span><span class="sxs-lookup"><span data-stu-id="378ef-133">It is crucial that your restore operation create sparse files with unallocated ranges rather than sparse files (or nonsparse files) initialized with zeroes.</span></span>

<span data-ttu-id="378ef-134">Observe que essa função não identificará necessariamente o arquivo de repositório comum ou os arquivos correspondentes a um conjunto de links do SIS na mídia de backup se esses arquivos ou arquivo de armazenamento comum ainda existirem no disco.</span><span class="sxs-lookup"><span data-stu-id="378ef-134">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common-store file or files still exist on disk.</span></span> <span data-ttu-id="378ef-135">O conteúdo de um fluxo de dados do arquivo de armazenamento comum nunca muda depois de ser criado, portanto, se o arquivo já existir no disco, não será necessário restaurá-lo.</span><span class="sxs-lookup"><span data-stu-id="378ef-135">The contents of a common-store file's data stream never changes once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="378ef-136">Os nomes de arquivos de repositório comuns são globalmente exclusivos para garantir a integridade da operação de restauração, mesmo que não ocorra no mesmo volume habilitado para SIS que a operação de backup tenha acessado.</span><span class="sxs-lookup"><span data-stu-id="378ef-136">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

## <a name="requirements"></a><span data-ttu-id="378ef-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="378ef-137">Requirements</span></span>



| <span data-ttu-id="378ef-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="378ef-138">Requirement</span></span> | <span data-ttu-id="378ef-139">Valor</span><span class="sxs-lookup"><span data-stu-id="378ef-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="378ef-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="378ef-140">Minimum supported client</span></span><br/> | <span data-ttu-id="378ef-141">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="378ef-141">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="378ef-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="378ef-142">Minimum supported server</span></span><br/> | <span data-ttu-id="378ef-143">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="378ef-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="378ef-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="378ef-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="378ef-145"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="378ef-145"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="378ef-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="378ef-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="378ef-147"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="378ef-147"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="378ef-148">DLL</span><span class="sxs-lookup"><span data-stu-id="378ef-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="378ef-149"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="378ef-149"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="378ef-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="378ef-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378ef-151">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="378ef-151">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="378ef-152">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="378ef-152">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> </dl>

 

