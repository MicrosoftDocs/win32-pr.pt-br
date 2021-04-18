---
title: Método SynchronizePublishingData da classe Win32_RDMSManagementData
description: Sincroniza o conjunto especificado de dados de publicação para os serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SynchronizePublishingData
- Método SynchronizePublishingData Serviços de Área de Trabalho Remota, classe Win32_RDMSManagementData
- Classe Win32_RDMSManagementData Serviços de Área de Trabalho Remota, método SynchronizePublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369565"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a><span data-ttu-id="f2288-106">Método SynchronizePublishingData da classe Win32 \_ RDMSManagementData</span><span class="sxs-lookup"><span data-stu-id="f2288-106">SynchronizePublishingData method of the Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="f2288-107">Sincroniza o conjunto especificado de dados de publicação para os serviços de gerenciamento de Área de Trabalho Remota (RDMS).</span><span class="sxs-lookup"><span data-stu-id="f2288-107">Synchronizes the specified set of publishing data for Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2288-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2288-108">Syntax</span></span>


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a><span data-ttu-id="f2288-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2288-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2288-110">*Contexto* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f2288-110">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2288-111">As informações de contexto dos dados de publicação a serem sincronizados.</span><span class="sxs-lookup"><span data-stu-id="f2288-111">The context information of the publishing data to synchronize.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2288-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2288-112">Return value</span></span>

<span data-ttu-id="f2288-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f2288-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2288-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2288-114">Requirements</span></span>



| <span data-ttu-id="f2288-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2288-115">Requirement</span></span> | <span data-ttu-id="f2288-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f2288-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2288-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2288-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2288-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f2288-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f2288-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2288-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2288-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2288-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f2288-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2288-121">Namespace</span></span><br/>                | <span data-ttu-id="f2288-122">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="f2288-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f2288-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f2288-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2288-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2288-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2288-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f2288-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2288-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2288-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f2288-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2288-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2288-128">**\_RDMSManagementData Win32**</span><span class="sxs-lookup"><span data-stu-id="f2288-128">**Win32\_RDMSManagementData**</span></span>](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





