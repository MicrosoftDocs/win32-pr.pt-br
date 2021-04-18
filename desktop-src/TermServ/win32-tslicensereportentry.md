---
title: Classe Win32_TSLicenseReportEntry
description: Fornece detalhes do Serviços de Área de Trabalho Remota emitido por licença de acesso para cliente por usuário (RDS \ 160; CAL por usuário).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportEntry classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369263"
---
# <a name="win32_tslicensereportentry-class"></a><span data-ttu-id="b4521-105">\_Classe Win32 TSLicenseReportEntry</span><span class="sxs-lookup"><span data-stu-id="b4521-105">Win32\_TSLicenseReportEntry class</span></span>

<span data-ttu-id="b4521-106">Fornece detalhes do Serviços de Área de Trabalho Remota emitido por licença de acesso para cliente por usuário (RDS CAL por usuário).</span><span class="sxs-lookup"><span data-stu-id="b4521-106">Provides details of the issued Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4521-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4521-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="b4521-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b4521-108">Members</span></span>

<span data-ttu-id="b4521-109">A classe **Win32 \_ TSLicenseReportEntry** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b4521-109">The **Win32\_TSLicenseReportEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="b4521-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b4521-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4521-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b4521-111">Properties</span></span>

<span data-ttu-id="b4521-112">A classe **Win32 \_ TSLicenseReportEntry** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b4521-112">The **Win32\_TSLicenseReportEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4521-113">**CALType**</span><span class="sxs-lookup"><span data-stu-id="b4521-113">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4521-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b4521-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4521-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b4521-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4521-116">Especifica o tipo de CAL emitida.</span><span class="sxs-lookup"><span data-stu-id="b4521-116">Specifies the type of CAL issued.</span></span> <span data-ttu-id="b4521-117">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4521-117">This will be one of the following values.</span></span>

<span data-ttu-id="b4521-118">**Windows server 2008 R2 e Windows server 2008:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b4521-118">**Windows Server 2008 R2 and Windows Server 2008:** This property is not supported.</span></span>

<span data-ttu-id="b4521-119">"Interno de TS por dispositivo CAL"</span><span class="sxs-lookup"><span data-stu-id="b4521-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="b4521-120">"TS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="b4521-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="b4521-121">"CAL do conector de Internet TS"</span><span class="sxs-lookup"><span data-stu-id="b4521-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="b4521-122">"TS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="b4521-122">"TS Per User CAL"</span></span>

<span data-ttu-id="b4521-123">"TS ou RDS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="b4521-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="b4521-124">"TS ou RDS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="b4521-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="b4521-125">"VDI Standard Suite por licença de assinatura de dispositivo"</span><span class="sxs-lookup"><span data-stu-id="b4521-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="b4521-126">"VDI Premium Suite por licença de assinatura de dispositivo"</span><span class="sxs-lookup"><span data-stu-id="b4521-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="b4521-127">"RDS CAL por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="b4521-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="b4521-128">"RDS CAL por usuário"</span><span class="sxs-lookup"><span data-stu-id="b4521-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="b4521-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="b4521-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4521-130">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4521-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b4521-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b4521-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4521-132">Data de validade da licença que foi emitida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b4521-132">Expiration date of the license that was issued to the user.</span></span>

</dd> <dt>

<span data-ttu-id="b4521-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="b4521-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4521-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b4521-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4521-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b4521-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4521-136">Versão do Serviços de Área de Trabalho Remota para a qual a CAL RDS por usuário foi emitida.</span><span class="sxs-lookup"><span data-stu-id="b4521-136">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="b4521-137">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="b4521-137">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="b4521-138">Somente os servidores que executam o Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="b4521-138">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="b4521-139">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="b4521-139">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="b4521-140">Somente os servidores que executam o Windows Server 2008 R2 ou o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="b4521-140">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="b4521-141">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="b4521-141">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="b4521-142">Somente servidores que executam o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="b4521-142">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4521-143">**ProductVersionid**</span><span class="sxs-lookup"><span data-stu-id="b4521-143">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4521-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4521-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4521-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b4521-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4521-146">Identificador de versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b4521-146">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="b4521-147">4</span><span class="sxs-lookup"><span data-stu-id="b4521-147">4</span></span>
</dt> <dd>

<span data-ttu-id="b4521-148">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4521-148">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="b4521-149">3</span><span class="sxs-lookup"><span data-stu-id="b4521-149">3</span></span>
</dt> <dd>

<span data-ttu-id="b4521-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4521-150">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="b4521-151">2</span><span class="sxs-lookup"><span data-stu-id="b4521-151">2</span></span>
</dt> <dd>

<span data-ttu-id="b4521-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4521-152">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="b4521-153">1</span><span class="sxs-lookup"><span data-stu-id="b4521-153">1</span></span>
</dt> <dd>

<span data-ttu-id="b4521-154">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="b4521-154">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b4521-155">0</span><span class="sxs-lookup"><span data-stu-id="b4521-155">0</span></span>
</dt> <dd>

<span data-ttu-id="b4521-156">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="b4521-156">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4521-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="b4521-157">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4521-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b4521-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4521-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b4521-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4521-160">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b4521-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b4521-161">Nome do usuário para o qual a licença foi emitida.</span><span class="sxs-lookup"><span data-stu-id="b4521-161">Name of the user to whom the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4521-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4521-162">Remarks</span></span>

<span data-ttu-id="b4521-163">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="b4521-163">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="b4521-164">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b4521-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b4521-165">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b4521-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b4521-166">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b4521-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b4521-167">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b4521-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4521-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4521-168">Requirements</span></span>



| <span data-ttu-id="b4521-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4521-169">Requirement</span></span> | <span data-ttu-id="b4521-170">Valor</span><span class="sxs-lookup"><span data-stu-id="b4521-170">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4521-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4521-171">Minimum supported client</span></span><br/> | <span data-ttu-id="b4521-172">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b4521-172">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b4521-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4521-173">Minimum supported server</span></span><br/> | <span data-ttu-id="b4521-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4521-174">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b4521-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4521-175">Namespace</span></span><br/>                | <span data-ttu-id="b4521-176">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b4521-176">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b4521-177">MOF</span><span class="sxs-lookup"><span data-stu-id="b4521-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4521-178"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4521-178"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4521-179">DLL</span><span class="sxs-lookup"><span data-stu-id="b4521-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4521-180"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4521-180"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4521-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4521-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4521-182">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="b4521-182">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="b4521-183">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="b4521-183">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="b4521-184">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="b4521-184">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="b4521-185">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="b4521-185">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="b4521-186">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b4521-186">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

