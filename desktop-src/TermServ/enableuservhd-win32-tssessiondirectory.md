---
title: Método EnableUserVhd da classe Win32_TSSessionDirectory
description: Habilita um VHD de perfil de usuário em um servidor RDSH.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableUserVhd
- Método EnableUserVhd Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método EnableUserVhd
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757937"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="2912b-106">Método EnableUserVhd da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="2912b-106">EnableUserVhd method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="2912b-107">Habilita um VHD de perfil de usuário em um servidor RDSH.</span><span class="sxs-lookup"><span data-stu-id="2912b-107">Enables a user profile VHD on an RDSH server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2912b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2912b-108">Syntax</span></span>


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a><span data-ttu-id="2912b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2912b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2912b-110">*UvhdShareUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2912b-110">*UvhdShareUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2912b-111">O local do compartilhamento onde todos os VHDs de perfil de usuário são armazenados.</span><span class="sxs-lookup"><span data-stu-id="2912b-111">The location of the share where all user profile VHDs are stored.</span></span>

</dd> <dt>

<span data-ttu-id="2912b-112">*UvhdRoamingPolicyXml* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2912b-112">*UvhdRoamingPolicyXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2912b-113">A política de roaming para o VHD do perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="2912b-113">The roaming policy for the user profile VHD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2912b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2912b-114">Requirements</span></span>



| <span data-ttu-id="2912b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2912b-115">Requirement</span></span> | <span data-ttu-id="2912b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2912b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2912b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2912b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2912b-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2912b-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2912b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2912b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2912b-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2912b-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="2912b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2912b-121">Namespace</span></span><br/>                | <span data-ttu-id="2912b-122">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2912b-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2912b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="2912b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2912b-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2912b-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2912b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2912b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2912b-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2912b-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2912b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2912b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2912b-128">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="2912b-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





