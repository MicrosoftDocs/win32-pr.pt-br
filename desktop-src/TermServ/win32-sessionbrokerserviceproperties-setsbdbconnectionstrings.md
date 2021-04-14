---
title: Método SetSBDbConnectionStrings da classe Win32_SessionBrokerServiceProperties
description: Salva as cadeias de conexão do BD, primária e secundária, no registro.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSBDbConnectionStrings
- Método SetSBDbConnectionStrings Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método SetSBDbConnectionStrings
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455136"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="14c93-106">Método SetSBDbConnectionStrings da classe Win32 \_ SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="14c93-106">SetSBDbConnectionStrings method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="14c93-107">Salva as cadeias de conexão do BD, primária e secundária, no registro.</span><span class="sxs-lookup"><span data-stu-id="14c93-107">Saves DB connection strings, both primary and secondary, in the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c93-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14c93-108">Syntax</span></span>


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="14c93-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14c93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c93-110">*connStringToCentralDBRdcms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14c93-110">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c93-111">A cadeia de conexão primária.</span><span class="sxs-lookup"><span data-stu-id="14c93-111">The primary connection string.</span></span>

</dd> <dt>

<span data-ttu-id="14c93-112">*secondaryConnStringToCentralDBRdcms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14c93-112">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c93-113">A cadeia de conexão secundária.</span><span class="sxs-lookup"><span data-stu-id="14c93-113">The secondary connection string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14c93-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14c93-114">Requirements</span></span>



| <span data-ttu-id="14c93-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c93-115">Requirement</span></span> | <span data-ttu-id="14c93-116">Valor</span><span class="sxs-lookup"><span data-stu-id="14c93-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14c93-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14c93-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14c93-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="14c93-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="14c93-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14c93-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14c93-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="14c93-120">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="14c93-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="14c93-121">Namespace</span></span><br/>                | <span data-ttu-id="14c93-122">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="14c93-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="14c93-123">MOF</span><span class="sxs-lookup"><span data-stu-id="14c93-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14c93-124"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14c93-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="14c93-125">DLL</span><span class="sxs-lookup"><span data-stu-id="14c93-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14c93-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14c93-126"><dt>RDMS.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="14c93-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="14c93-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c93-128">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="14c93-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





