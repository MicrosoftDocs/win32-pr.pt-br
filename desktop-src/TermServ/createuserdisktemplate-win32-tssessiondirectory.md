---
title: Método CreateUserDiskTemplate da classe Win32_TSSessionDirectory
description: Cria um modelo de disco de usuário.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CreateUserDiskTemplate
- Método CreateUserDiskTemplate Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método CreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085272"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="53d63-106">Método CreateUserDiskTemplate da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="53d63-106">CreateUserDiskTemplate method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="53d63-107">Cria um modelo de disco de usuário.</span><span class="sxs-lookup"><span data-stu-id="53d63-107">Creates a user disk template.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d63-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53d63-108">Syntax</span></span>


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="53d63-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53d63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d63-110">*UserDisksStorageUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53d63-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d63-111">O local do compartilhamento onde todos os discos de usuário são armazenados.</span><span class="sxs-lookup"><span data-stu-id="53d63-111">The location of the share where all user disks are stored.</span></span>

</dd> <dt>

<span data-ttu-id="53d63-112">*UserDiskMaxSizeInGB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53d63-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d63-113">O tamanho máximo em gigabytes, para todos os discos de usuário.</span><span class="sxs-lookup"><span data-stu-id="53d63-113">The maximum size in gigabytes, for all user disks.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53d63-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53d63-114">Requirements</span></span>



| <span data-ttu-id="53d63-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="53d63-115">Requirement</span></span> | <span data-ttu-id="53d63-116">Valor</span><span class="sxs-lookup"><span data-stu-id="53d63-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53d63-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53d63-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53d63-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="53d63-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="53d63-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53d63-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53d63-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53d63-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="53d63-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="53d63-121">Namespace</span></span><br/>                | <span data-ttu-id="53d63-122">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="53d63-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="53d63-123">MOF</span><span class="sxs-lookup"><span data-stu-id="53d63-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53d63-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53d63-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="53d63-125">DLL</span><span class="sxs-lookup"><span data-stu-id="53d63-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53d63-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53d63-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53d63-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="53d63-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d63-128">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="53d63-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





