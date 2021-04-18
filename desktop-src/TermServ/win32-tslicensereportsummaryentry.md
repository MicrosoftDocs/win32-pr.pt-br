---
title: Classe Win32_TSLicenseReportSummaryEntry
description: Fornece um resumo das licenças de acesso para cliente de Serviços de Área de Trabalho Remota instaladas e emitidas por usuário (RDS \ 160; CALs por usuário).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportSummaryEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportSummaryEntry classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811903"
---
# <a name="win32_tslicensereportsummaryentry-class"></a><span data-ttu-id="2865d-105">\_Classe Win32 TSLicenseReportSummaryEntry</span><span class="sxs-lookup"><span data-stu-id="2865d-105">Win32\_TSLicenseReportSummaryEntry class</span></span>

<span data-ttu-id="2865d-106">Fornece um resumo das licenças de acesso para cliente de Serviços de Área de Trabalho Remota instaladas e emitidas por usuário (RDS CALs por usuário).</span><span class="sxs-lookup"><span data-stu-id="2865d-106">Provides a summary of the installed and issued Remote Desktop Services Per User client access licenses (RDS Per User CALs).</span></span>

## <a name="syntax"></a><span data-ttu-id="2865d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2865d-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a><span data-ttu-id="2865d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2865d-108">Members</span></span>

<span data-ttu-id="2865d-109">A classe **Win32 \_ TSLicenseReportSummaryEntry** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2865d-109">The **Win32\_TSLicenseReportSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="2865d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2865d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2865d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2865d-111">Properties</span></span>

<span data-ttu-id="2865d-112">A classe **Win32 \_ TSLicenseReportSummaryEntry** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2865d-112">The **Win32\_TSLicenseReportSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2865d-113">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="2865d-113">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2865d-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2865d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2865d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2865d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2865d-116">Número de CALs por usuário do RDS que estão instaladas.</span><span class="sxs-lookup"><span data-stu-id="2865d-116">Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-117">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="2865d-117">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2865d-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2865d-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2865d-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2865d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2865d-120">Número de CALs de RDS por usuário que são emitidas.</span><span class="sxs-lookup"><span data-stu-id="2865d-120">Number of RDS Per User CALs that are issued.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-121">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="2865d-121">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2865d-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2865d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2865d-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2865d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2865d-124">Versão do Serviços de Área de Trabalho Remota para a qual a CAL RDS por usuário foi emitida.</span><span class="sxs-lookup"><span data-stu-id="2865d-124">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="2865d-125">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="2865d-125">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-126">Somente os servidores que executam o Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="2865d-126">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-127">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="2865d-127">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-128">Somente os servidores que executam o Windows Server 2008 R2 ou o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="2865d-128">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-129">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="2865d-129">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-130">Somente servidores que executam o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="2865d-130">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2865d-131">**ProductVersionid**</span><span class="sxs-lookup"><span data-stu-id="2865d-131">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2865d-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2865d-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2865d-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2865d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2865d-134">Identificador de versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="2865d-134">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="2865d-135">4</span><span class="sxs-lookup"><span data-stu-id="2865d-135">4</span></span>
</dt> <dd>

<span data-ttu-id="2865d-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2865d-136">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="2865d-137">3</span><span class="sxs-lookup"><span data-stu-id="2865d-137">3</span></span>
</dt> <dd>

<span data-ttu-id="2865d-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2865d-138">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="2865d-139">2</span><span class="sxs-lookup"><span data-stu-id="2865d-139">2</span></span>
</dt> <dd>

<span data-ttu-id="2865d-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2865d-140">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="2865d-141">1</span><span class="sxs-lookup"><span data-stu-id="2865d-141">1</span></span>
</dt> <dd>

<span data-ttu-id="2865d-142">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="2865d-142">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-143">0</span><span class="sxs-lookup"><span data-stu-id="2865d-143">0</span></span>
</dt> <dd>

<span data-ttu-id="2865d-144">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="2865d-144">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2865d-145">**TSCALAvailability**</span><span class="sxs-lookup"><span data-stu-id="2865d-145">**TSCALAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2865d-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2865d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2865d-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2865d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2865d-148">A disponibilidade das CALs de RDS por usuário.</span><span class="sxs-lookup"><span data-stu-id="2865d-148">The availability of the RDS Per User CALs.</span></span> <span data-ttu-id="2865d-149">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2865d-149">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="2865d-150">Há</span><span class="sxs-lookup"><span data-stu-id="2865d-150">"Available"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-151">As CALs do RDS por usuário estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2865d-151">The RDS Per User CALs are available.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-152">Certo</span><span class="sxs-lookup"><span data-stu-id="2865d-152">"Limited"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-153">A disponibilidade das CALs de RDS por usuário é limitada.</span><span class="sxs-lookup"><span data-stu-id="2865d-153">The availability of the RDS Per User CALs is limited.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-154">"None"</span><span class="sxs-lookup"><span data-stu-id="2865d-154">"None"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-155">As CALs do RDS por usuário não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2865d-155">The RDS Per User CALs are not available.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-156">"Sem rastreamento"</span><span class="sxs-lookup"><span data-stu-id="2865d-156">"Not Tracking"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-157">A disponibilidade das CALs de RDS por usuário não está sendo acompanhada.</span><span class="sxs-lookup"><span data-stu-id="2865d-157">The availability of the RDS Per User CALs is not being tracked.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2865d-158">**TSCALType**</span><span class="sxs-lookup"><span data-stu-id="2865d-158">**TSCALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2865d-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2865d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2865d-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2865d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2865d-161">O tipo de RDS CALs por usuário.</span><span class="sxs-lookup"><span data-stu-id="2865d-161">The type of RDS Per User CALs.</span></span> <span data-ttu-id="2865d-162">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2865d-162">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="2865d-163">"Por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="2865d-163">"Per Device"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-164">As CALs do RDS por usuário são emitidas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2865d-164">The RDS Per User CALs are issued per device.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-165">"Por usuário"</span><span class="sxs-lookup"><span data-stu-id="2865d-165">"Per User"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-166">As CALs do RDS por usuário são emitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="2865d-166">The RDS Per User CALs are issued per user.</span></span>

</dd> <dt>

<span data-ttu-id="2865d-167">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="2865d-167">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="2865d-168">O tipo de RDS CALs por usuário é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2865d-168">The type of RDS Per User CALs is unknown.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2865d-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2865d-169">Requirements</span></span>



| <span data-ttu-id="2865d-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="2865d-170">Requirement</span></span> | <span data-ttu-id="2865d-171">Valor</span><span class="sxs-lookup"><span data-stu-id="2865d-171">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2865d-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2865d-172">Minimum supported client</span></span><br/> | <span data-ttu-id="2865d-173">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2865d-173">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2865d-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2865d-174">Minimum supported server</span></span><br/> | <span data-ttu-id="2865d-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2865d-175">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2865d-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="2865d-176">Namespace</span></span><br/>                | <span data-ttu-id="2865d-177">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2865d-177">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2865d-178">MOF</span><span class="sxs-lookup"><span data-stu-id="2865d-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2865d-179"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2865d-179"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2865d-180">DLL</span><span class="sxs-lookup"><span data-stu-id="2865d-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2865d-181"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2865d-181"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



 

 





