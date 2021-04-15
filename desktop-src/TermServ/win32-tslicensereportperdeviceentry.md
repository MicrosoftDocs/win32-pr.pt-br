---
title: Classe Win32_TSLicenseReportPerDeviceEntry
description: Fornece detalhes sobre a Serviços de Área de Trabalho Remota com falha por licença de acesso para cliente por dispositivo (RDS \ 160; CAL por dispositivo).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportPerDeviceEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportPerDeviceEntry classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454728"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a><span data-ttu-id="e5479-105">\_Classe Win32 TSLicenseReportPerDeviceEntry</span><span class="sxs-lookup"><span data-stu-id="e5479-105">Win32\_TSLicenseReportPerDeviceEntry class</span></span>

<span data-ttu-id="e5479-106">Fornece detalhes sobre o Serviços de Área de Trabalho Remota com falha por licença de acesso para cliente por dispositivo (RDS CAL por dispositivo).</span><span class="sxs-lookup"><span data-stu-id="e5479-106">Provides details about the failed Remote Desktop Services Per Device client access license (RDS Per Device CAL).</span></span>

<span data-ttu-id="e5479-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e5479-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5479-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5479-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="e5479-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e5479-109">Members</span></span>

<span data-ttu-id="e5479-110">A classe **Win32 \_ TSLicenseReportPerDeviceEntry** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e5479-110">The **Win32\_TSLicenseReportPerDeviceEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="e5479-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5479-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5479-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5479-112">Properties</span></span>

<span data-ttu-id="e5479-113">A classe **Win32 \_ TSLicenseReportPerDeviceEntry** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e5479-113">The **Win32\_TSLicenseReportPerDeviceEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5479-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="e5479-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5479-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5479-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5479-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5479-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5479-117">Especifica o tipo de CAL emitida.</span><span class="sxs-lookup"><span data-stu-id="e5479-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="e5479-118">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5479-118">This will be one of the following values.</span></span>

<span data-ttu-id="e5479-119">"Interno de TS por dispositivo CAL"</span><span class="sxs-lookup"><span data-stu-id="e5479-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="e5479-120">"TS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="e5479-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="e5479-121">"CAL do conector de Internet TS"</span><span class="sxs-lookup"><span data-stu-id="e5479-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="e5479-122">"TS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="e5479-122">"TS Per User CAL"</span></span>

<span data-ttu-id="e5479-123">"TS ou RDS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="e5479-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="e5479-124">"TS ou RDS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="e5479-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="e5479-125">"VDI Standard Suite por licença de assinatura de dispositivo"</span><span class="sxs-lookup"><span data-stu-id="e5479-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="e5479-126">"VDI Premium Suite por licença de assinatura de dispositivo"</span><span class="sxs-lookup"><span data-stu-id="e5479-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="e5479-127">"RDS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="e5479-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="e5479-128">"RDS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="e5479-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="e5479-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="e5479-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5479-130">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5479-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e5479-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5479-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5479-132">A data de validade da licença.</span><span class="sxs-lookup"><span data-stu-id="e5479-132">The expiration date of the license.</span></span>

</dd> <dt>

<span data-ttu-id="e5479-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="e5479-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5479-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5479-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5479-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5479-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5479-136">A versão do Serviços de Área de Trabalho Remota para a qual a CAL RDS por usuário foi emitida.</span><span class="sxs-lookup"><span data-stu-id="e5479-136">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="e5479-137">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5479-137">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="e5479-138">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="e5479-138">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="e5479-139">Somente os servidores que executam o Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="e5479-139">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="e5479-140">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="e5479-140">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="e5479-141">Somente os servidores que executam o Windows Server 2008 R2 ou o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="e5479-141">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="e5479-142">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="e5479-142">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="e5479-143">Somente servidores que executam o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="e5479-143">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5479-144">**ProductVersionid**</span><span class="sxs-lookup"><span data-stu-id="e5479-144">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5479-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5479-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5479-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5479-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5479-147">Identificador de versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="e5479-147">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="e5479-148">4</span><span class="sxs-lookup"><span data-stu-id="e5479-148">4</span></span>
</dt> <dd>

<span data-ttu-id="e5479-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5479-149">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="e5479-150">3</span><span class="sxs-lookup"><span data-stu-id="e5479-150">3</span></span>
</dt> <dd>

<span data-ttu-id="e5479-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5479-151">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="e5479-152">2</span><span class="sxs-lookup"><span data-stu-id="e5479-152">2</span></span>
</dt> <dd>

<span data-ttu-id="e5479-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5479-153">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="e5479-154">1</span><span class="sxs-lookup"><span data-stu-id="e5479-154">1</span></span>
</dt> <dd>

<span data-ttu-id="e5479-155">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="e5479-155">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e5479-156">0</span><span class="sxs-lookup"><span data-stu-id="e5479-156">0</span></span>
</dt> <dd>

<span data-ttu-id="e5479-157">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="e5479-157">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5479-158">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="e5479-158">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5479-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5479-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5479-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5479-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5479-161">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e5479-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e5479-162">O identificador de hardware do computador.</span><span class="sxs-lookup"><span data-stu-id="e5479-162">The hardware identifier of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="e5479-163">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="e5479-163">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5479-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5479-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5479-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5479-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5479-166">O nome do computador para o qual a emissão de licença foi tentada.</span><span class="sxs-lookup"><span data-stu-id="e5479-166">The name of the computer that the license issuance was attempted for.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5479-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5479-167">Requirements</span></span>



| <span data-ttu-id="e5479-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5479-168">Requirement</span></span> | <span data-ttu-id="e5479-169">Valor</span><span class="sxs-lookup"><span data-stu-id="e5479-169">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5479-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5479-170">Minimum supported client</span></span><br/> | <span data-ttu-id="e5479-171">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e5479-171">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e5479-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5479-172">Minimum supported server</span></span><br/> | <span data-ttu-id="e5479-173">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5479-173">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="e5479-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5479-174">Namespace</span></span><br/>                | <span data-ttu-id="e5479-175">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e5479-175">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e5479-176">MOF</span><span class="sxs-lookup"><span data-stu-id="e5479-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5479-177"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5479-177"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5479-178">DLL</span><span class="sxs-lookup"><span data-stu-id="e5479-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5479-179"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5479-179"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5479-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5479-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5479-181">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="e5479-181">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

