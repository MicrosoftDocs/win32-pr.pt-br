---
title: Função SisCreateBackupStructure (Sisbkup. h)
description: Cria uma estrutura de backup do SIS com base nas informações fornecidas.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Backup de função SisCreateBackupStructure
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454883"
---
# <a name="siscreatebackupstructure-function"></a><span data-ttu-id="04e7d-104">Função SisCreateBackupStructure</span><span class="sxs-lookup"><span data-stu-id="04e7d-104">SisCreateBackupStructure function</span></span>

<span data-ttu-id="04e7d-105">A função **SisCreateBackupStructure** cria uma estrutura de backup do SIS com base nas informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="04e7d-105">The **SisCreateBackupStructure** function creates a SIS backup structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e7d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04e7d-106">Syntax</span></span>


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="04e7d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04e7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e7d-108">*volumeRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04e7d-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e7d-109">Nome do arquivo da raiz do volume, sem a barra invertida à direita, do volume cujo backup será feito.</span><span class="sxs-lookup"><span data-stu-id="04e7d-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="04e7d-110">Por exemplo, especifique "C:" e não "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="04e7d-110">For example, specify "C:" and not "C:\\".</span></span>

</dd> <dt>

<span data-ttu-id="04e7d-111">*sisBackupStructure* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04e7d-111">*sisBackupStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04e7d-112">A estrutura de backup do SIS foi retornada.</span><span class="sxs-lookup"><span data-stu-id="04e7d-112">Returned SIS backup structure.</span></span>

</dd> <dt>

<span data-ttu-id="04e7d-113">*commonStoreRootPathname* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04e7d-113">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04e7d-114">Nome do caminho totalmente qualificado do repositório comum do volume especificado.</span><span class="sxs-lookup"><span data-stu-id="04e7d-114">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="04e7d-115">Por exemplo, "c: \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="04e7d-115">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="04e7d-116">*countOfCommonStoreFilesToBackUp* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04e7d-116">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04e7d-117">Número de arquivos listados no parâmetro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="04e7d-117">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="04e7d-118">*commonStoreFilesToBackUp* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04e7d-118">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04e7d-119">Ponteiro para uma matriz de nomes de arquivo que especifica uma lista de arquivos internos usados pelo SIS para gerenciar o volume especificado.</span><span class="sxs-lookup"><span data-stu-id="04e7d-119">Pointer to an array of file names that specifies a list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="04e7d-120">Esses arquivos devem ser armazenados em backup ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comuns solicitados pelo [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span><span class="sxs-lookup"><span data-stu-id="04e7d-120">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e7d-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04e7d-121">Return value</span></span>

<span data-ttu-id="04e7d-122">Essa função retornará **true** se for concluída com êxito e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="04e7d-122">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="04e7d-123">Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="04e7d-123">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="04e7d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="04e7d-124">Remarks</span></span>

<span data-ttu-id="04e7d-125">Essa função cria uma estrutura de backup do SIS, que é usada pela API de backup do SIS para criar e manter uma lista de links de arquivos no volume e nos arquivos originais aos quais os links apontam.</span><span class="sxs-lookup"><span data-stu-id="04e7d-125">This function creates a SIS backup structure, which is used by the SIS backup API to create and maintain a list of the file links on the volume and the original files the links point to.</span></span> <span data-ttu-id="04e7d-126">Essa função deve ser chamada apenas uma vez para cada volume habilitado para SIS que está sendo submetido a backup.</span><span class="sxs-lookup"><span data-stu-id="04e7d-126">This function should be called only once for each SIS-enabled volume being backed up.</span></span> <span data-ttu-id="04e7d-127">Todos os arquivos no volume especificado devem ser tratados como arquivos de armazenamento comum e armazenados em backup somente se o SIS indicar que deveria.</span><span class="sxs-lookup"><span data-stu-id="04e7d-127">All files within the specified volume should be treated as common-store files and backed up only if SIS indicates that they should.</span></span>

<span data-ttu-id="04e7d-128">Os parâmetros *countOfCommonStoreFilesToBackUp* e *commonStoreFilesToBackUp* juntos retornam uma lista de arquivos que devem ser copiados em backup, independentemente de quais links são incluídos no backup.</span><span class="sxs-lookup"><span data-stu-id="04e7d-128">The *countOfCommonStoreFilesToBackUp* and *commonStoreFilesToBackUp* parameters together return a list of files that must be backed up regardless of which links are backed up.</span></span>

<span data-ttu-id="04e7d-129">Se *countOfCommonStoreFilesToBackUp* for 0, *commonStoreFilesToBackUp* poderá ser um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="04e7d-129">If *countOfCommonStoreFilesToBackUp* is 0, *commonStoreFilesToBackUp* may be a **NULL** pointer.</span></span> <span data-ttu-id="04e7d-130">O valor do parâmetro *commonStoreFilesToBackUp* deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="04e7d-130">The value of the *commonStoreFilesToBackUp* parameter should be ignored.</span></span>

<span data-ttu-id="04e7d-131">Depois que a operação de backup for concluída, Desaloque a memória usada pela matriz *commonStoreFilesToBackUp* de cadeias de caracteres chamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="04e7d-131">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04e7d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04e7d-132">Requirements</span></span>



| <span data-ttu-id="04e7d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="04e7d-133">Requirement</span></span> | <span data-ttu-id="04e7d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="04e7d-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04e7d-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04e7d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="04e7d-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="04e7d-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="04e7d-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04e7d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="04e7d-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04e7d-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04e7d-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04e7d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="04e7d-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="04e7d-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="04e7d-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04e7d-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="04e7d-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04e7d-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="04e7d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="04e7d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04e7d-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04e7d-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04e7d-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="04e7d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e7d-146">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="04e7d-146">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="04e7d-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="04e7d-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="04e7d-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="04e7d-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> </dl>

 

