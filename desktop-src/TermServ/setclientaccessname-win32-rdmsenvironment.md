---
title: Método SetClientAccessName da classe Win32_RDMSEnvironment
description: Atualiza o nome do registro de recurso (DNS) do sistema de nomes de domínio (RR) de um ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetClientAccessName
- Método SetClientAccessName Serviços de Área de Trabalho Remota, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Serviços de Área de Trabalho Remota, método SetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753323"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="fa36d-106">Método SetClientAccessName da classe Win32 \_ RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="fa36d-106">SetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="fa36d-107">Atualiza o nome do registro de recurso (DNS) do sistema de nomes de domínio (RR) de um ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="fa36d-107">Updates the Domain Name System (DNS) resource record (RR) name of an Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa36d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa36d-108">Syntax</span></span>


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="fa36d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa36d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa36d-110">*ClientAccessName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa36d-110">*ClientAccessName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa36d-111">O nome do novo RR.</span><span class="sxs-lookup"><span data-stu-id="fa36d-111">The new RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa36d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa36d-112">Return value</span></span>

<span data-ttu-id="fa36d-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="fa36d-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa36d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa36d-114">Requirements</span></span>



| <span data-ttu-id="fa36d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa36d-115">Requirement</span></span> | <span data-ttu-id="fa36d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fa36d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa36d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa36d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa36d-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fa36d-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fa36d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa36d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa36d-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa36d-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fa36d-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa36d-121">Namespace</span></span><br/>                | <span data-ttu-id="fa36d-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="fa36d-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fa36d-123">MOF</span><span class="sxs-lookup"><span data-stu-id="fa36d-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa36d-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa36d-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa36d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fa36d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa36d-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa36d-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fa36d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa36d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa36d-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="fa36d-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





