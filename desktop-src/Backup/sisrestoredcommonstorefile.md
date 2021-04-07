---
title: Função SisRestoredCommonStoreFile (Sisbkup. h)
description: Relata para a arquitetura do SIS que um arquivo de armazenamento comum foi gravado.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Backup de função SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918177"
---
# <a name="sisrestoredcommonstorefile-function"></a><span data-ttu-id="4cd1c-104">Função SisRestoredCommonStoreFile</span><span class="sxs-lookup"><span data-stu-id="4cd1c-104">SisRestoredCommonStoreFile function</span></span>

<span data-ttu-id="4cd1c-105">A função **SisRestoredCommonStoreFile** relata para a arquitetura do SIS que um arquivo de armazenamento comum foi gravado.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-105">The **SisRestoredCommonStoreFile** function reports to the SIS architecture that a common-store file has been written.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd1c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cd1c-106">Syntax</span></span>


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a><span data-ttu-id="4cd1c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cd1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd1c-108">*sisRestoreStructure* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cd1c-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd1c-109">Ponteiro para uma estrutura de restauração do SIS retornada de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="4cd1c-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="4cd1c-110">*commonStoreFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4cd1c-110">*commonStoreFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd1c-111">Nome do arquivo de repositório comum restaurado.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-111">Name of the restored common-store file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd1c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cd1c-112">Return value</span></span>

<span data-ttu-id="4cd1c-113">Essa função retornará **true** se for concluída com êxito e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-113">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="4cd1c-114">Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-114">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cd1c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cd1c-115">Remarks</span></span>

<span data-ttu-id="4cd1c-116">Essa função deve ser chamada depois que você tiver restaurado um arquivo de repositório comum.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-116">This function should be called after you have restored a common-store file.</span></span> <span data-ttu-id="4cd1c-117">Ele notifica a arquitetura do SIS que um novo arquivo de armazenamento comum foi gravado, para que a arquitetura do SIS possa executar tarefas de manutenção internas, como inicializar suas estruturas de dados internas ou corrigir os links para o arquivo de repositório comum.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-117">It notifies the SIS architecture that a new common-store file has been written, so that the SIS architecture can perform internal maintenance tasks such as initializing its internal data structures or fixing the links to the common-store file.</span></span>

<span data-ttu-id="4cd1c-118">A operação de restauração deve restaurar somente os arquivos de repositório comuns relatados pelo [**SisRestoredLink**](sisrestoredlink.md), mesmo se houver arquivos de repositório comum adicionais na mídia de backup.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-118">Your restore operation should restore only common-store files reported by [**SisRestoredLink**](sisrestoredlink.md), even if there are additional common-store files on the backup media.</span></span> <span data-ttu-id="4cd1c-119">A operação de restauração pode restaurar os links do SIS e os arquivos de armazenamento comum em qualquer ordem escolhida; no entanto, ele deve chamar **SisRestoredLink** depois de restaurar qualquer link e deve chamar essa função depois de restaurar qualquer arquivo de repositório comum.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-119">Your restore operation can restore the SIS links and common-store files in any order it chooses; however, it must call **SisRestoredLink** after it restores any link, and it must call this function after it restores any common-store file.</span></span> <span data-ttu-id="4cd1c-120">Como a operação de restauração não pode identificar quais arquivos de armazenamento comum serão restaurados até que os nomes de arquivo sejam relatados a ele como resultado da restauração de um link, a operação de restauração sempre restaurará um arquivo de repositório comum depois que pelo menos um link fizer referência a ele for restaurado.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-120">Because your restore operation cannot identify which common-store files will be restored until the file names are reported to it as a result of restoring a link, your restore operation will always restore a common-store file after at least one link referring to it is restored.</span></span> <span data-ttu-id="4cd1c-121">No entanto, você pode restaurar outros links do SIS que apontam para o arquivo de armazenamento comum.</span><span class="sxs-lookup"><span data-stu-id="4cd1c-121">However, you can then restore additional SIS links that point to that common-store file.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd1c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cd1c-122">Requirements</span></span>



| <span data-ttu-id="4cd1c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cd1c-123">Requirement</span></span> | <span data-ttu-id="4cd1c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4cd1c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd1c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cd1c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd1c-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4cd1c-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4cd1c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cd1c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd1c-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4cd1c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4cd1c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cd1c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cd1c-130"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-130"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cd1c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cd1c-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="4cd1c-132"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-132"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="4cd1c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4cd1c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cd1c-134"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cd1c-134"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd1c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cd1c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd1c-136">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="4cd1c-136">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="4cd1c-137">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="4cd1c-137">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

