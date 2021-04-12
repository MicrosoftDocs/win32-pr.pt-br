---
title: Método SetActiveServer da classe Win32_RDMSEnvironment
description: Define o FQDN do ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS) para o nó atual.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetActiveServer
- Método SetActiveServer Serviços de Área de Trabalho Remota, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Serviços de Área de Trabalho Remota, método SetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455047"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="f115c-106">Método SetActiveServer da classe Win32 \_ RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="f115c-106">SetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="f115c-107">Define o FQDN do ambiente de serviços de gerenciamento de Área de Trabalho Remota (RDMS) para o nó atual.</span><span class="sxs-lookup"><span data-stu-id="f115c-107">Sets the FQDN of the Remote Desktop Management Services (RDMS) environment to the current node.</span></span>

## <a name="syntax"></a><span data-ttu-id="f115c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f115c-108">Syntax</span></span>


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a><span data-ttu-id="f115c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f115c-109">Parameters</span></span>

<span data-ttu-id="f115c-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f115c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f115c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f115c-111">Return value</span></span>

<span data-ttu-id="f115c-112">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f115c-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f115c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f115c-113">Requirements</span></span>



| <span data-ttu-id="f115c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f115c-114">Requirement</span></span> | <span data-ttu-id="f115c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f115c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f115c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f115c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f115c-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f115c-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f115c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f115c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f115c-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f115c-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f115c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="f115c-120">Namespace</span></span><br/>                | <span data-ttu-id="f115c-121">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="f115c-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f115c-122">MOF</span><span class="sxs-lookup"><span data-stu-id="f115c-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f115c-123"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f115c-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f115c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f115c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f115c-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f115c-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f115c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f115c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f115c-127">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="f115c-127">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





