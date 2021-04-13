---
title: Classe Win32_TSLicenseReportFailedPerUserEntry
description: Fornece detalhes sobre a licença de acesso para cliente de Serviços de Área de Trabalho Remota por usuário com falha (RDS \ 160; CAL por usuário).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportFailedPerUserEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportFailedPerUserEntry classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369262"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a><span data-ttu-id="3e644-105">\_Classe Win32 TSLicenseReportFailedPerUserEntry</span><span class="sxs-lookup"><span data-stu-id="3e644-105">Win32\_TSLicenseReportFailedPerUserEntry class</span></span>

<span data-ttu-id="3e644-106">Fornece detalhes sobre a licença de acesso para cliente de Serviços de Área de Trabalho Remota por usuário com falha (RDS CAL por usuário).</span><span class="sxs-lookup"><span data-stu-id="3e644-106">Provides details about the failed Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

<span data-ttu-id="3e644-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3e644-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e644-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e644-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="3e644-109">Membros</span><span class="sxs-lookup"><span data-stu-id="3e644-109">Members</span></span>

<span data-ttu-id="3e644-110">A classe **Win32 \_ TSLicenseReportFailedPerUserEntry** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3e644-110">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="3e644-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e644-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e644-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e644-112">Properties</span></span>

<span data-ttu-id="3e644-113">A classe **Win32 \_ TSLicenseReportFailedPerUserEntry** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e644-113">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e644-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="3e644-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e644-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e644-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e644-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e644-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e644-117">Especifica o tipo de CAL emitida.</span><span class="sxs-lookup"><span data-stu-id="3e644-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="3e644-118">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e644-118">This will be one of the following values.</span></span>

<span data-ttu-id="3e644-119">"Interno de TS por dispositivo CAL"</span><span class="sxs-lookup"><span data-stu-id="3e644-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="3e644-120">"TS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="3e644-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="3e644-121">"CAL do conector de Internet TS"</span><span class="sxs-lookup"><span data-stu-id="3e644-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="3e644-122">"TS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="3e644-122">"TS Per User CAL"</span></span>

<span data-ttu-id="3e644-123">"TS ou RDS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="3e644-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="3e644-124">"TS ou RDS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="3e644-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="3e644-125">"VDI Standard Suite por licença de assinatura de dispositivo"</span><span class="sxs-lookup"><span data-stu-id="3e644-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="3e644-126">"VDI Premium Suite por licença de assinatura de dispositivo"</span><span class="sxs-lookup"><span data-stu-id="3e644-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="3e644-127">"RDS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="3e644-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="3e644-128">"RDS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="3e644-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="3e644-129">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="3e644-129">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e644-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e644-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e644-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e644-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e644-132">A versão do Serviços de Área de Trabalho Remota para a qual a CAL RDS por usuário foi emitida.</span><span class="sxs-lookup"><span data-stu-id="3e644-132">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="3e644-133">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e644-133">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="3e644-134">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="3e644-134">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="3e644-135">Somente os servidores que executam o Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="3e644-135">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="3e644-136">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="3e644-136">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="3e644-137">Somente os servidores que executam o Windows Server 2008 R2 ou o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="3e644-137">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="3e644-138">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="3e644-138">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="3e644-139">Somente servidores que executam o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="3e644-139">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3e644-140">**ProductVersionid**</span><span class="sxs-lookup"><span data-stu-id="3e644-140">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e644-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e644-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e644-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e644-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e644-143">Identificador de versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="3e644-143">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="3e644-144">4</span><span class="sxs-lookup"><span data-stu-id="3e644-144">4</span></span>
</dt> <dd>

<span data-ttu-id="3e644-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e644-145">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="3e644-146">3</span><span class="sxs-lookup"><span data-stu-id="3e644-146">3</span></span>
</dt> <dd>

<span data-ttu-id="3e644-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e644-147">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="3e644-148">2</span><span class="sxs-lookup"><span data-stu-id="3e644-148">2</span></span>
</dt> <dd>

<span data-ttu-id="3e644-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e644-149">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="3e644-150">1</span><span class="sxs-lookup"><span data-stu-id="3e644-150">1</span></span>
</dt> <dd>

<span data-ttu-id="3e644-151">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="3e644-151">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3e644-152">0</span><span class="sxs-lookup"><span data-stu-id="3e644-152">0</span></span>
</dt> <dd>

<span data-ttu-id="3e644-153">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="3e644-153">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3e644-154">**TriedIssuanceOn**</span><span class="sxs-lookup"><span data-stu-id="3e644-154">**TriedIssuanceOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e644-155">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3e644-155">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="3e644-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e644-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e644-157">A data em que foi tentada a emissão da licença.</span><span class="sxs-lookup"><span data-stu-id="3e644-157">The date on which license issuance was attempted.</span></span>

</dd> <dt>

<span data-ttu-id="3e644-158">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="3e644-158">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e644-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e644-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e644-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e644-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e644-161">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e644-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e644-162">O nome do usuário para o qual a emissão de licença foi tentada.</span><span class="sxs-lookup"><span data-stu-id="3e644-162">The name of the user to whom the license issuance was attempted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e644-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e644-163">Requirements</span></span>



| <span data-ttu-id="3e644-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e644-164">Requirement</span></span> | <span data-ttu-id="3e644-165">Valor</span><span class="sxs-lookup"><span data-stu-id="3e644-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e644-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e644-166">Minimum supported client</span></span><br/> | <span data-ttu-id="3e644-167">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3e644-167">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3e644-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e644-168">Minimum supported server</span></span><br/> | <span data-ttu-id="3e644-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e644-169">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="3e644-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e644-170">Namespace</span></span><br/>                | <span data-ttu-id="3e644-171">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3e644-171">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3e644-172">MOF</span><span class="sxs-lookup"><span data-stu-id="3e644-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e644-173"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e644-173"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e644-174">DLL</span><span class="sxs-lookup"><span data-stu-id="3e644-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e644-175"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e644-175"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e644-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e644-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e644-177">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="3e644-177">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

