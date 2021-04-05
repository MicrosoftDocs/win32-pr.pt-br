---
title: Método SetBrokerHAMode da classe Win32_SessionBrokerServiceProperties
description: Migra os dados de um banco de dado de WID local para o novo banco de dados baseado em SQL Server. Ele também configura o servidor do agente para usar o SQL Server central.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetBrokerHAMode
- Método SetBrokerHAMode Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método SetBrokerHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085553"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="6d9d1-107">Método SetBrokerHAMode da classe Win32 \_ SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="6d9d1-107">SetBrokerHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="6d9d1-108">Migra os dados de um banco de dado de WID local para o novo banco de dados baseado em SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6d9d1-108">Migrates data from a local WID database to the new SQL server-based database.</span></span> <span data-ttu-id="6d9d1-109">Ele também configura o servidor do agente para usar o SQL Server central.</span><span class="sxs-lookup"><span data-stu-id="6d9d1-109">It also configures the broker server to use the central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9d1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d9d1-110">Syntax</span></span>


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="6d9d1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d9d1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d9d1-112">*connStringToCentralDBRdcms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9d1-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9d1-113">Cadeia de conexão para o banco de dados central.</span><span class="sxs-lookup"><span data-stu-id="6d9d1-113">Connection string to the central database.</span></span>

</dd> <dt>

<span data-ttu-id="6d9d1-114">*secondaryConnStringToCentralDBRdcms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9d1-114">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9d1-115">Cadeia de conexão secundária para o banco de dados central.</span><span class="sxs-lookup"><span data-stu-id="6d9d1-115">Secondary connection string to the central database.</span></span>

<span data-ttu-id="6d9d1-116">**Windows server 2012 R2 e Windows server 2012:** Esse parâmetro não está disponível antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="6d9d1-116">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="6d9d1-117">*brokerDnsRRName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9d1-117">*brokerDnsRRName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9d1-118">Nome DNS do agente.</span><span class="sxs-lookup"><span data-stu-id="6d9d1-118">Broker DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="6d9d1-119">*activeBrokerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d9d1-119">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d9d1-120">Nome do agente ativo.</span><span class="sxs-lookup"><span data-stu-id="6d9d1-120">Active broker name.</span></span>

<span data-ttu-id="6d9d1-121">**Windows server 2012 R2 e Windows server 2012:** Esse parâmetro não está disponível antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="6d9d1-121">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d9d1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d9d1-122">Requirements</span></span>



| <span data-ttu-id="6d9d1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d9d1-123">Requirement</span></span> | <span data-ttu-id="6d9d1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6d9d1-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9d1-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d9d1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9d1-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6d9d1-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6d9d1-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d9d1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9d1-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d9d1-128">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="6d9d1-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d9d1-129">Namespace</span></span><br/>                | <span data-ttu-id="6d9d1-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6d9d1-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="6d9d1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6d9d1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d9d1-132"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d9d1-132"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d9d1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6d9d1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d9d1-134"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d9d1-134"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9d1-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d9d1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9d1-136">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="6d9d1-136">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





