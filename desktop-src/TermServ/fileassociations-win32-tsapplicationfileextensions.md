---
title: Método fileassociações da classe Win32_TSApplicationFileExtensions
description: Examina o registro para obter as associações de arquivo atuais para um aplicativo.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Método fileassociationes Serviços de Área de Trabalho Remota
- Método fileassociationes Serviços de Área de Trabalho Remota, classe Win32_TSApplicationFileExtensions
- Classe de Win32_TSApplicationFileExtensions Serviços de Área de Trabalho Remota, método FileAssociations
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105767729"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="6cdb1-106">Método FileAssociations da classe Win32 \_ TSApplicationFileExtensions</span><span class="sxs-lookup"><span data-stu-id="6cdb1-106">FileAssociations method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="6cdb1-107">Examina o registro para obter as associações de arquivo atuais para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cdb1-107">Scans the registry to get the current file associations for an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cdb1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cdb1-108">Syntax</span></span>


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a><span data-ttu-id="6cdb1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cdb1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cdb1-110">*AppPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cdb1-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdb1-111">Especifica o caminho para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cdb1-111">Specifies the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="6cdb1-112">*Associações* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="6cdb1-112">*FileAssociations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cdb1-113">Após a conclusão bem-sucedida, contém as associações de arquivo para este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cdb1-113">On successful completion contains the file associations for this application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6cdb1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cdb1-114">Requirements</span></span>



| <span data-ttu-id="6cdb1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cdb1-115">Requirement</span></span> | <span data-ttu-id="6cdb1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6cdb1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdb1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cdb1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6cdb1-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6cdb1-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6cdb1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cdb1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6cdb1-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6cdb1-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="6cdb1-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="6cdb1-121">Namespace</span></span><br/>                | <span data-ttu-id="6cdb1-122">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6cdb1-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6cdb1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6cdb1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cdb1-124"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cdb1-124"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="6cdb1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6cdb1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cdb1-126"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cdb1-126"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cdb1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cdb1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cdb1-128">**\_TSApplicationFileExtensions Win32**</span><span class="sxs-lookup"><span data-stu-id="6cdb1-128">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> <dt>

[<span data-ttu-id="6cdb1-129">**\_RDFileAssociation Win32**</span><span class="sxs-lookup"><span data-stu-id="6cdb1-129">**Win32\_RDFileAssociation**</span></span>](win32-rdfileassociation.md)
</dt> </dl>

 

 





