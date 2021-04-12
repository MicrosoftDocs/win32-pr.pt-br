---
title: Método IsDbReachable da classe Win32_SessionBrokerServiceProperties
description: Verifica se o banco de dados está acessível.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsDbReachable
- Método IsDbReachable Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455137"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="ea795-106">Método IsDbReachable da classe Win32 \_ SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="ea795-106">IsDbReachable method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="ea795-107">Verifica se o banco de dados está acessível.</span><span class="sxs-lookup"><span data-stu-id="ea795-107">Checks if the database is reachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea795-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea795-108">Syntax</span></span>


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="ea795-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea795-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea795-110">*connStringToDb* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea795-110">*connStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea795-111">A cadeia de conexão para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ea795-111">The connection string to the database.</span></span>

</dd> <dt>

<span data-ttu-id="ea795-112">*connSecondaryStringToDb* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea795-112">*connSecondaryStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea795-113">Cadeia de conexão secundária para o banco de dados central.</span><span class="sxs-lookup"><span data-stu-id="ea795-113">Secondary connection string to the central database.</span></span>

<span data-ttu-id="ea795-114">**Windows server 2012 R2 e Windows server 2012:** Esse parâmetro não está disponível antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ea795-114">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="ea795-115">*activeBrokerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ea795-115">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea795-116">Nome do agente ativo.</span><span class="sxs-lookup"><span data-stu-id="ea795-116">Active broker name.</span></span>

<span data-ttu-id="ea795-117">**Windows server 2012 R2 e Windows server 2012:** Esse parâmetro não está disponível antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ea795-117">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea795-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea795-118">Requirements</span></span>



| <span data-ttu-id="ea795-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea795-119">Requirement</span></span> | <span data-ttu-id="ea795-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ea795-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea795-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea795-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea795-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ea795-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ea795-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea795-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea795-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ea795-124">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="ea795-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea795-125">Namespace</span></span><br/>                | <span data-ttu-id="ea795-126">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ea795-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="ea795-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ea795-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea795-128"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea795-128"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea795-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ea795-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea795-130"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea795-130"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea795-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea795-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea795-132">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="ea795-132">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





