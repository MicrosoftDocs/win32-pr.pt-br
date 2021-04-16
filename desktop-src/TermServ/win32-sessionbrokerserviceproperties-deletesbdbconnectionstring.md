---
title: Método DeleteSBDbConnectionString da classe Win32_SessionBrokerServiceProperties
description: Exclui cadeias de conexão de BD (primárias ou secundárias) do registro.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeleteSBDbConnectionString
- Método DeleteSBDbConnectionString Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método DeleteSBDbConnectionString
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757587"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="94a8b-106">Método DeleteSBDbConnectionString da classe Win32 \_ SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="94a8b-106">DeleteSBDbConnectionString method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="94a8b-107">Exclui cadeias de conexão de BD (primárias ou secundárias) do registro.</span><span class="sxs-lookup"><span data-stu-id="94a8b-107">Deletes DB connection strings (primary or secondary) from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a8b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94a8b-108">Syntax</span></span>


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a><span data-ttu-id="94a8b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94a8b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94a8b-110">*IsSecondaryConnString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94a8b-110">*IsSecondaryConnString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94a8b-111">Se **for true**, a cadeia de conexão secundária será removida.</span><span class="sxs-lookup"><span data-stu-id="94a8b-111">If **True**, secondary connection string is removed.</span></span> <span data-ttu-id="94a8b-112">Se **for false**, a cadeia de conexão primária será removida.</span><span class="sxs-lookup"><span data-stu-id="94a8b-112">If **False**, primary connection string is removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94a8b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94a8b-113">Requirements</span></span>



| <span data-ttu-id="94a8b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="94a8b-114">Requirement</span></span> | <span data-ttu-id="94a8b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="94a8b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94a8b-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94a8b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="94a8b-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="94a8b-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="94a8b-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94a8b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="94a8b-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="94a8b-119">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="94a8b-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="94a8b-120">Namespace</span></span><br/>                | <span data-ttu-id="94a8b-121">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="94a8b-121">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="94a8b-122">MOF</span><span class="sxs-lookup"><span data-stu-id="94a8b-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94a8b-123"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94a8b-123"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="94a8b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="94a8b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94a8b-125"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94a8b-125"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94a8b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="94a8b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a8b-127">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="94a8b-127">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





