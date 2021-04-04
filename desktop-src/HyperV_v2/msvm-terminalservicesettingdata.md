---
description: Representa as configurações dos serviços de terminal do computador virtual em um host.
ms.assetid: 1f8d0718-09da-4231-95eb-cc63b6f324dd
title: Classe Msvm_TerminalServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalServiceSettingData
- Msvm_TerminalServiceSettingData.InstanceID
- Msvm_TerminalServiceSettingData.Caption
- Msvm_TerminalServiceSettingData.Description
- Msvm_TerminalServiceSettingData.ElementName
- Msvm_TerminalServiceSettingData.ListenerPort
- Msvm_TerminalServiceSettingData.DisableSelfSignedCertificateGeneration
- Msvm_TerminalServiceSettingData.AuthCertificateHash
- Msvm_TerminalServiceSettingData.TrustedIssuerCertificateHashes
- Msvm_TerminalServiceSettingData.AllowedHashAlgorithms
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27d98971c847eab5042823e8a1524051a15fd679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647664"
---
# <a name="msvm_terminalservicesettingdata-class"></a><span data-ttu-id="2acbb-103">\_Classe Msvm TerminalServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="2acbb-103">Msvm\_TerminalServiceSettingData class</span></span>

<span data-ttu-id="2acbb-104">Representa as configurações dos serviços de terminal do computador virtual em um host.</span><span class="sxs-lookup"><span data-stu-id="2acbb-104">Represents the settings for the virtual computer terminal services on a host.</span></span> <span data-ttu-id="2acbb-105">As propriedades desta classe não podem ser modificadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="2acbb-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="2acbb-106">O cliente deve chamar o método [**Msvm \_ TerminalService. ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) para modificar qualquer uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2acbb-106">The client must call the [**Msvm\_TerminalService.ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="2acbb-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2acbb-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2acbb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2acbb-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Hyper-V Terminal Service Settings";
  string  Description = "Settings for the Hyper-V Terminal Service";
  string  ElementName = "Hyper-V Terminal Service Settings";
  uint32  ListenerPort;
  boolean DisableSelfSignedCertificateGeneration;
  uint8   AuthCertificateHash[];
  string  TrustedIssuerCertificateHashes[];
  string  AllowedHashAlgorithms[];
};
```

## <a name="members"></a><span data-ttu-id="2acbb-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2acbb-109">Members</span></span>

<span data-ttu-id="2acbb-110">A classe **Msvm \_ TerminalServiceSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2acbb-110">The **Msvm\_TerminalServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2acbb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2acbb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2acbb-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2acbb-112">Properties</span></span>

<span data-ttu-id="2acbb-113">A classe **Msvm \_ TerminalServiceSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2acbb-113">The **Msvm\_TerminalServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2acbb-114">**AllowedHashAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="2acbb-114">**AllowedHashAlgorithms**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-115">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2acbb-115">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-117">A lista de algoritmos de hash aceitas para verificar a assinatura de tokens de autenticação federada.</span><span class="sxs-lookup"><span data-stu-id="2acbb-117">The list of hash algorithms accepted for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="2acbb-118">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2acbb-118">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="2acbb-119">**AuthCertificateHash**</span><span class="sxs-lookup"><span data-stu-id="2acbb-119">**AuthCertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-120">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="2acbb-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-122">O hash do certificado a ser usado para autenticação remota.</span><span class="sxs-lookup"><span data-stu-id="2acbb-122">The hash of the certificate to use for remote authentication.</span></span>

</dd> <dt>

<span data-ttu-id="2acbb-123">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="2acbb-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2acbb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-126">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="2acbb-126">A short description of the object.</span></span> <span data-ttu-id="2acbb-127">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2acbb-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2acbb-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2acbb-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2acbb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-131">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="2acbb-131">A description of the object.</span></span> <span data-ttu-id="2acbb-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2acbb-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2acbb-133">**DisableSelfSignedCertificateGeneration**</span><span class="sxs-lookup"><span data-stu-id="2acbb-133">**DisableSelfSignedCertificateGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2acbb-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-136">Desabilita a geração de certificado autoassinado.</span><span class="sxs-lookup"><span data-stu-id="2acbb-136">Disables self-signed certificate generation.</span></span>

</dd> <dt>

<span data-ttu-id="2acbb-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2acbb-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2acbb-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-140">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="2acbb-140">A display name for the object.</span></span> <span data-ttu-id="2acbb-141">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2acbb-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2acbb-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2acbb-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2acbb-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-145">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="2acbb-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-146">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="2acbb-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2acbb-147">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2acbb-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2acbb-148">**ListenerPort**</span><span class="sxs-lookup"><span data-stu-id="2acbb-148">**ListenerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2acbb-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-151">A porta de rede na qual a conexão inicial da sessão remota será feita.</span><span class="sxs-lookup"><span data-stu-id="2acbb-151">The network port on which the initial remote session connection will be made.</span></span>

</dd> <dt>

<span data-ttu-id="2acbb-152">**TrustedIssuerCertificateHashes**</span><span class="sxs-lookup"><span data-stu-id="2acbb-152">**TrustedIssuerCertificateHashes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2acbb-153">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2acbb-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2acbb-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2acbb-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2acbb-155">A lista de hashes de certificado de emissor confiável para verificar a assinatura de tokens de autenticação federada.</span><span class="sxs-lookup"><span data-stu-id="2acbb-155">The list of trusted issuer certificate hashes for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="2acbb-156">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2acbb-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2acbb-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2acbb-157">Requirements</span></span>



| <span data-ttu-id="2acbb-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="2acbb-158">Requirement</span></span> | <span data-ttu-id="2acbb-159">Valor</span><span class="sxs-lookup"><span data-stu-id="2acbb-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acbb-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2acbb-160">Minimum supported client</span></span><br/> | <span data-ttu-id="2acbb-161">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2acbb-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2acbb-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2acbb-162">Minimum supported server</span></span><br/> | <span data-ttu-id="2acbb-163">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2acbb-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2acbb-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="2acbb-164">Namespace</span></span><br/>                | <span data-ttu-id="2acbb-165">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2acbb-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2acbb-166">MOF</span><span class="sxs-lookup"><span data-stu-id="2acbb-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2acbb-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2acbb-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2acbb-168">DLL</span><span class="sxs-lookup"><span data-stu-id="2acbb-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2acbb-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2acbb-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

