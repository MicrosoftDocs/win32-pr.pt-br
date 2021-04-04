---
title: Função SisCreateRestoreStructure (Sisbkup. h)
description: Cria uma estrutura de restauração do SIS com base nas informações fornecidas.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Backup de função SisCreateRestoreStructure
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824275"
---
# <a name="siscreaterestorestructure-function"></a><span data-ttu-id="2f921-104">Função SisCreateRestoreStructure</span><span class="sxs-lookup"><span data-stu-id="2f921-104">SisCreateRestoreStructure function</span></span>

<span data-ttu-id="2f921-105">A função **SisCreateRestoreStructure** cria uma estrutura de restauração do SIS com base nas informações fornecidas.</span><span class="sxs-lookup"><span data-stu-id="2f921-105">The **SisCreateRestoreStructure** function creates a SIS restore structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f921-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f921-106">Syntax</span></span>


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="2f921-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f921-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f921-108">*volumeRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f921-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f921-109">Nome do arquivo da raiz do volume, sem a barra invertida à direita, do volume cujo backup será feito.</span><span class="sxs-lookup"><span data-stu-id="2f921-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="2f921-110">Por exemplo, especifique "C:" e não "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="2f921-110">For example, specify "C:" and not "C:\\".</span></span> <span data-ttu-id="2f921-111">O volume não pode ser o volume do sistema ou de inicialização.</span><span class="sxs-lookup"><span data-stu-id="2f921-111">The volume cannot be the system or boot volume.</span></span>

</dd> <dt>

<span data-ttu-id="2f921-112">*sisRestoreStructure* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2f921-112">*sisRestoreStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f921-113">Foi retornada a estrutura de restauração do SIS.</span><span class="sxs-lookup"><span data-stu-id="2f921-113">Returned SIS restore structure.</span></span> <span data-ttu-id="2f921-114">Essa estrutura deve ser tratada como opaca pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="2f921-114">This structure should be treated as opaque by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="2f921-115">*commonStoreRootPathname* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2f921-115">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f921-116">Nome do caminho totalmente qualificado do repositório comum do volume especificado.</span><span class="sxs-lookup"><span data-stu-id="2f921-116">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="2f921-117">Por exemplo, "c: \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="2f921-117">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="2f921-118">*countOfCommonStoreFilesToRestore* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2f921-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f921-119">Número de arquivos listados no parâmetro *commonStoreFilesToRestore* .</span><span class="sxs-lookup"><span data-stu-id="2f921-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2f921-120">*commonStoreFilesToRestore* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2f921-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f921-121">Ponteiro para uma matriz de nomes de arquivo que especifica a lista de arquivos internos usados pelo SIS para gerenciar o volume especificado.</span><span class="sxs-lookup"><span data-stu-id="2f921-121">Pointer to an array of file names that specifies the list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="2f921-122">Esses arquivos devem ser restaurados ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comuns solicitados pelo [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="2f921-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f921-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f921-123">Return value</span></span>

<span data-ttu-id="2f921-124">Essa função retornará **true** se for concluída com êxito e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2f921-124">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="2f921-125">Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="2f921-125">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f921-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f921-126">Remarks</span></span>

<span data-ttu-id="2f921-127">Essa função estabelece o ambiente de restauração no volume especificado no modo como o [**SisCreateBackupStructure**](siscreatebackupstructure.md) estabelece o ambiente de backup no volume especificado.</span><span class="sxs-lookup"><span data-stu-id="2f921-127">This function establishes the restore environment on the specified volume in the way that [**SisCreateBackupStructure**](siscreatebackupstructure.md) establishes the backup environment on the specified volume.</span></span>

<span data-ttu-id="2f921-128">Observe que essa função não identificará necessariamente o arquivo de repositório comum ou os arquivos correspondentes a um conjunto de links do SIS na mídia de backup se esses arquivos ou arquivo de armazenamento comuns ainda existirem no disco.</span><span class="sxs-lookup"><span data-stu-id="2f921-128">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common store file or files still exist on disk.</span></span> <span data-ttu-id="2f921-129">O conteúdo de um fluxo de dados do arquivo de armazenamento comum nunca muda depois de ser criado, portanto, se o arquivo já existir no disco, não será necessário restaurá-lo.</span><span class="sxs-lookup"><span data-stu-id="2f921-129">The contents of a common-store file's data stream never change once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="2f921-130">Os nomes de arquivos de repositório comuns são globalmente exclusivos para garantir a integridade da operação de restauração, mesmo que não ocorra no mesmo volume habilitado para SIS que a operação de backup tenha acessado.</span><span class="sxs-lookup"><span data-stu-id="2f921-130">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

<span data-ttu-id="2f921-131">Depois que a operação de restauração for concluída, Desaloque a memória usada pela matriz *commonStoreFilesToRestore* de cadeias de caracteres chamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="2f921-131">After the restore operation is complete, deallocate the memory used by the *commonStoreFilesToRestore* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f921-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f921-132">Requirements</span></span>



| <span data-ttu-id="2f921-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f921-133">Requirement</span></span> | <span data-ttu-id="2f921-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2f921-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f921-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f921-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f921-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2f921-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2f921-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f921-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f921-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f921-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2f921-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f921-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f921-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f921-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f921-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f921-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f921-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f921-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f921-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2f921-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f921-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f921-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f921-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f921-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f921-146">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="2f921-146">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="2f921-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="2f921-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="2f921-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="2f921-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="2f921-149">**SisFreeBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="2f921-149">**SisFreeBackupStructure**</span></span>](sisfreebackupstructure.md)
</dt> </dl>

 

