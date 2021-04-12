---
title: Método GetActiveServer da classe Win32_RDMSEnvironment
description: Recupera o FQDN (nome de domínio totalmente qualificado) do ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetActiveServer
- Método GetActiveServer Serviços de Área de Trabalho Remota, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Serviços de Área de Trabalho Remota, método GetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455393"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="647a4-106">Método GetActiveServer da classe Win32 \_ RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="647a4-106">GetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="647a4-107">Recupera o FQDN (nome de domínio totalmente qualificado) do ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="647a4-107">Retrieves the fully qualified domain name (FQDN) of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="647a4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="647a4-108">Syntax</span></span>


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="647a4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="647a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="647a4-110">*Nome do Server* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="647a4-110">*ServerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="647a4-111">Recebe o FQDN recuperado.</span><span class="sxs-lookup"><span data-stu-id="647a4-111">Receives the retrieved FQDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="647a4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="647a4-112">Return value</span></span>

<span data-ttu-id="647a4-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="647a4-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="647a4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="647a4-114">Requirements</span></span>



| <span data-ttu-id="647a4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="647a4-115">Requirement</span></span> | <span data-ttu-id="647a4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="647a4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="647a4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="647a4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="647a4-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="647a4-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="647a4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="647a4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="647a4-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="647a4-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="647a4-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="647a4-121">Namespace</span></span><br/>                | <span data-ttu-id="647a4-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="647a4-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="647a4-123">MOF</span><span class="sxs-lookup"><span data-stu-id="647a4-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="647a4-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="647a4-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="647a4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="647a4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="647a4-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="647a4-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="647a4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="647a4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="647a4-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="647a4-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





