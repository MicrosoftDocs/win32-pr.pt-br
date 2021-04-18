---
title: Método SetBrokerNonHAMode da classe Win32_SessionBrokerServiceProperties
description: Migra dados do SQL Server central para um banco de dado local. Ele também configura o servidor do agente para usar o banco de dados local.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetBrokerNonHAMode
- Método SetBrokerNonHAMode Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método SetBrokerNonHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788023"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="51fda-107">Método SetBrokerNonHAMode da classe Win32 \_ SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="51fda-107">SetBrokerNonHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="51fda-108">Migra dados do SQL Server central para um banco de dado local.</span><span class="sxs-lookup"><span data-stu-id="51fda-108">Migrates data from central SQL Server to a local database.</span></span> <span data-ttu-id="51fda-109">Ele também configura o servidor do agente para usar o banco de dados local.</span><span class="sxs-lookup"><span data-stu-id="51fda-109">It also configures the broker server to use the local database.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fda-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51fda-110">Syntax</span></span>


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="51fda-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51fda-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51fda-112">*connStringToCentralDBRdcms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51fda-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51fda-113">Cadeia de conexão para o banco de dados central.</span><span class="sxs-lookup"><span data-stu-id="51fda-113">Connection string to the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51fda-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51fda-114">Requirements</span></span>



| <span data-ttu-id="51fda-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="51fda-115">Requirement</span></span> | <span data-ttu-id="51fda-116">Valor</span><span class="sxs-lookup"><span data-stu-id="51fda-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51fda-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51fda-117">Minimum supported client</span></span><br/> | <span data-ttu-id="51fda-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="51fda-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="51fda-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51fda-119">Minimum supported server</span></span><br/> | <span data-ttu-id="51fda-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51fda-120">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="51fda-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="51fda-121">Namespace</span></span><br/>                | <span data-ttu-id="51fda-122">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="51fda-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="51fda-123">MOF</span><span class="sxs-lookup"><span data-stu-id="51fda-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51fda-124"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51fda-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="51fda-125">DLL</span><span class="sxs-lookup"><span data-stu-id="51fda-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51fda-126"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51fda-126"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51fda-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="51fda-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fda-128">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="51fda-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





