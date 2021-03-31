---
title: Classe Win32_TSLicenseReportFailedPerUserSummaryEntry
description: Fornece detalhes dos domínios para os quais a emissão por usuário falhou.
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportFailedPerUserSummaryEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportFailedPerUserSummaryEntry classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918048"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a><span data-ttu-id="53a19-105">\_Classe Win32 TSLicenseReportFailedPerUserSummaryEntry</span><span class="sxs-lookup"><span data-stu-id="53a19-105">Win32\_TSLicenseReportFailedPerUserSummaryEntry class</span></span>

<span data-ttu-id="53a19-106">Fornece detalhes dos domínios para os quais a emissão por usuário falhou.</span><span class="sxs-lookup"><span data-stu-id="53a19-106">Provides details of the domains to which Per User Issuance was failed.</span></span>

<span data-ttu-id="53a19-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="53a19-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a19-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53a19-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a><span data-ttu-id="53a19-109">Membros</span><span class="sxs-lookup"><span data-stu-id="53a19-109">Members</span></span>

<span data-ttu-id="53a19-110">A classe **Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="53a19-110">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="53a19-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="53a19-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53a19-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="53a19-112">Properties</span></span>

<span data-ttu-id="53a19-113">A classe **Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="53a19-113">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53a19-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="53a19-114">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a19-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53a19-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53a19-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53a19-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a19-117">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="53a19-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="53a19-118">Especifica o nome de domínio para o qual a emissão de licença falhou.</span><span class="sxs-lookup"><span data-stu-id="53a19-118">Specifies the domain name to which the license issuance failed.</span></span>

</dd> <dt>

<span data-ttu-id="53a19-119">**FailedIssuanceCount**</span><span class="sxs-lookup"><span data-stu-id="53a19-119">**FailedIssuanceCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a19-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53a19-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53a19-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53a19-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53a19-122">O número de emissões com falha.</span><span class="sxs-lookup"><span data-stu-id="53a19-122">The number of failed issuances.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53a19-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53a19-123">Requirements</span></span>



| <span data-ttu-id="53a19-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="53a19-124">Requirement</span></span> | <span data-ttu-id="53a19-125">Valor</span><span class="sxs-lookup"><span data-stu-id="53a19-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a19-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53a19-126">Minimum supported client</span></span><br/> | <span data-ttu-id="53a19-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="53a19-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="53a19-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53a19-128">Minimum supported server</span></span><br/> | <span data-ttu-id="53a19-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53a19-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="53a19-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="53a19-130">Namespace</span></span><br/>                | <span data-ttu-id="53a19-131">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="53a19-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="53a19-132">MOF</span><span class="sxs-lookup"><span data-stu-id="53a19-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53a19-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53a19-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="53a19-134">DLL</span><span class="sxs-lookup"><span data-stu-id="53a19-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53a19-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53a19-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a19-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="53a19-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a19-137">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="53a19-137">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 

