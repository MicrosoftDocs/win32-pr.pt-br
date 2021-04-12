---
title: Classe Win32_TSLicenseKeyPack
description: Fornece métodos e propriedades para exibir e instalar Serviços de Área de Trabalho Remota pacotes de chaves de licença.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseKeyPack classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499249"
---
# <a name="win32_tslicensekeypack-class"></a><span data-ttu-id="48e96-105">\_Classe Win32 TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="48e96-105">Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="48e96-106">Fornece métodos e propriedades para exibir e instalar Serviços de Área de Trabalho Remota pacotes de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="48e96-106">Provides methods and properties for viewing and installing Remote Desktop Services license key packs.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e96-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48e96-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a><span data-ttu-id="48e96-108">Membros</span><span class="sxs-lookup"><span data-stu-id="48e96-108">Members</span></span>

<span data-ttu-id="48e96-109">A classe **Win32 \_ TSLicenseKeyPack** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="48e96-109">The **Win32\_TSLicenseKeyPack** class has these types of members:</span></span>

-   [<span data-ttu-id="48e96-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="48e96-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="48e96-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48e96-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48e96-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="48e96-112">Methods</span></span>

<span data-ttu-id="48e96-113">A classe **Win32 \_ TSLicenseKeyPack** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="48e96-113">The **Win32\_TSLicenseKeyPack** class has these methods.</span></span>



| <span data-ttu-id="48e96-114">Método</span><span class="sxs-lookup"><span data-stu-id="48e96-114">Method</span></span>                                                                                                        | <span data-ttu-id="48e96-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="48e96-115">Description</span></span>                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e96-116">**ConvertLicenses**</span><span class="sxs-lookup"><span data-stu-id="48e96-116">**ConvertLicenses**</span></span>](convertlicenses-win32-tslicensekeypack.md)                                             | <span data-ttu-id="48e96-117">Converte as licenças no pacote de chaves atual.</span><span class="sxs-lookup"><span data-stu-id="48e96-117">Converts the licenses in the current key pack.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="48e96-118">**ImportAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-118">**ImportAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | <span data-ttu-id="48e96-119">Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="48e96-119">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/> |
| [<span data-ttu-id="48e96-120">**ImportLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="48e96-120">**ImportLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | <span data-ttu-id="48e96-121">Importações, de outro servidor de licença Área de Trabalho Remota, um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa um identificador de licença que foi recebido pela Internet ou pelo telefone.</span><span class="sxs-lookup"><span data-stu-id="48e96-121">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span><br/>                                               |
| [<span data-ttu-id="48e96-122">**ImportOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-122">**ImportOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | <span data-ttu-id="48e96-123">Importações, de outro servidor de licença Área de Trabalho Remota, uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="48e96-123">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="48e96-124">**ImportRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-124">**ImportRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | <span data-ttu-id="48e96-125">Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.</span><span class="sxs-lookup"><span data-stu-id="48e96-125">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                   |
| [<span data-ttu-id="48e96-126">**InstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-126">**InstallAgreementLicenseKeyPack**</span></span>](installagreementlicensekeypack-win32-tslicensekeypack.md)               | <span data-ttu-id="48e96-127">Instala um pacote de chaves de licença Serviços de Área de Trabalho Remota que foi adquirido por meio de uma licença de contrato.</span><span class="sxs-lookup"><span data-stu-id="48e96-127">Installs a Remote Desktop Services license key pack that was purchased through an agreement license.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="48e96-128">**InstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-128">**InstallLicenseKeyPack**</span></span>](installlicensekeypack-win32-tslicensekeypack.md)                                 | <span data-ttu-id="48e96-129">Instala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa uma ID de pacote de chaves de licença que foi recebida pela Internet ou pelo telefone.</span><span class="sxs-lookup"><span data-stu-id="48e96-129">Installs a Remote Desktop Services license key pack that uses a license key pack ID that was received over the Internet or the phone.</span></span><br/>                                                                                          |
| [<span data-ttu-id="48e96-130">**InstallOpenLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-130">**InstallOpenLicenseKeyPack**</span></span>](installopenlicensekeypack-win32-tslicensekeypack.md)                         | <span data-ttu-id="48e96-131">Instala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença aberto.</span><span class="sxs-lookup"><span data-stu-id="48e96-131">Installs a Remote Desktop Services license key pack that was purchased through an open license agreement.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="48e96-132">**InstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-132">**InstallRetailPurchaseLicenseKeyPack**</span></span>](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | <span data-ttu-id="48e96-133">Instala um pacote de chaves de licença Serviços de Área de Trabalho Remota que foi adquirido por meio de uma loja de varejo.</span><span class="sxs-lookup"><span data-stu-id="48e96-133">Installs a Remote Desktop Services license key pack that was purchased through a retail store.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="48e96-134">**ReinstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-134">**ReinstallAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | <span data-ttu-id="48e96-135">Reinstala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="48e96-135">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/>                                           |
| [<span data-ttu-id="48e96-136">**ReinstallLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="48e96-136">**ReinstallLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | <span data-ttu-id="48e96-137">Reinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.</span><span class="sxs-lookup"><span data-stu-id="48e96-137">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span><br/>                                                                                       |
| [<span data-ttu-id="48e96-138">**ReinstallOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-138">**ReinstallOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | <span data-ttu-id="48e96-139">Reinstala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="48e96-139">Reinstalls an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="48e96-140">**ReinstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-140">**ReinstallRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | <span data-ttu-id="48e96-141">Reinstala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.</span><span class="sxs-lookup"><span data-stu-id="48e96-141">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="48e96-142">**RemoveLicensesWithIdCount**</span><span class="sxs-lookup"><span data-stu-id="48e96-142">**RemoveLicensesWithIdCount**</span></span>](win32-tslicensekeypack-removelicenseswithidcount.md)                         | <span data-ttu-id="48e96-143">Remove o número especificado de licenças de Serviços de Área de Trabalho Remota do pacote de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="48e96-143">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="48e96-144">**UninstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="48e96-144">**UninstallLicenseKeyPack**</span></span>](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | <span data-ttu-id="48e96-145">Desinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-145">Uninstalls a Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="48e96-146">**UninstallLicenseKeyPackWithId**</span><span class="sxs-lookup"><span data-stu-id="48e96-146">**UninstallLicenseKeyPackWithId**</span></span>](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | <span data-ttu-id="48e96-147">Desinstala o pacote de chaves de licença Serviços de Área de Trabalho Remota com o identificador de pacote de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="48e96-147">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="48e96-148">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48e96-148">Properties</span></span>

<span data-ttu-id="48e96-149">A classe **Win32 \_ TSLicenseKeyPack** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="48e96-149">The **Win32\_TSLicenseKeyPack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48e96-150">**AccessRights**</span><span class="sxs-lookup"><span data-stu-id="48e96-150">**AccessRights**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48e96-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48e96-153">Qualificadores: [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**bitvalues**](/windows/desktop/WmiSdk/standard-qualifiers) ("sessão de RD", "sessão de VDI", "Calista", "parceiros de VDI")</span><span class="sxs-lookup"><span data-stu-id="48e96-153">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD Session", "VDI Session", "Calista", "VDI Partners")</span></span>
</dt> </dl>

<span data-ttu-id="48e96-154">Qualificador para direitos de acesso do pacote de chaves de Licenciamento TS</span><span class="sxs-lookup"><span data-stu-id="48e96-154">Qualifier for TS Licensing key pack access rights</span></span>

</dd> <dt>

<span data-ttu-id="48e96-155">**AvailableLicenses**</span><span class="sxs-lookup"><span data-stu-id="48e96-155">**AvailableLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-156">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48e96-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-158">Número total de licenças disponíveis no pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-158">Total number of available licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="48e96-159">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48e96-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48e96-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-162">Descrição do pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-162">Description of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="48e96-163">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="48e96-163">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-164">Tipo de dados: **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="48e96-164">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-166">A data de validade do pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-166">The expiration date of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="48e96-167">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="48e96-167">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48e96-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-170">Número total de licenças emitidas no pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-170">Total number of issued licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="48e96-171">**Pacote de chaves**</span><span class="sxs-lookup"><span data-stu-id="48e96-171">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48e96-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48e96-174">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="48e96-174">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="48e96-175">Identificador para o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-175">Identifier for the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="48e96-176">**Pacote de chaves**</span><span class="sxs-lookup"><span data-stu-id="48e96-176">**KeyPackType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48e96-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-179">Tipo de pacote de chaves para o servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-179">Type of key pack for the Remote Desktop license server.</span></span>

| <span data-ttu-id="48e96-180">Valor</span><span class="sxs-lookup"><span data-stu-id="48e96-180">Value</span></span> | <span data-ttu-id="48e96-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="48e96-181">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="48e96-182">0</span><span class="sxs-lookup"><span data-stu-id="48e96-182">0</span></span> | <span data-ttu-id="48e96-183">O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="48e96-183">The Remote Desktop Services license key pack type is unknown.</span></span> |
| <span data-ttu-id="48e96-184">1</span><span class="sxs-lookup"><span data-stu-id="48e96-184">1</span></span> | <span data-ttu-id="48e96-185">O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é uma compra de varejo.</span><span class="sxs-lookup"><span data-stu-id="48e96-185">The Remote Desktop Services license key pack type is a retail purchase.</span></span> |
| <span data-ttu-id="48e96-186">2</span><span class="sxs-lookup"><span data-stu-id="48e96-186">2</span></span> | <span data-ttu-id="48e96-187">O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é uma compra de volume.</span><span class="sxs-lookup"><span data-stu-id="48e96-187">The Remote Desktop Services license key pack type is a volume purchase.</span></span> |
| <span data-ttu-id="48e96-188">3</span><span class="sxs-lookup"><span data-stu-id="48e96-188">3</span></span> | <span data-ttu-id="48e96-189">O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é uma licença simultânea.</span><span class="sxs-lookup"><span data-stu-id="48e96-189">The Remote Desktop Services license key pack type is a concurrent license.</span></span> |
| <span data-ttu-id="48e96-190">4</span><span class="sxs-lookup"><span data-stu-id="48e96-190">4</span></span> | <span data-ttu-id="48e96-191">O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é temporário.</span><span class="sxs-lookup"><span data-stu-id="48e96-191">The Remote Desktop Services license key pack type is temporary.</span></span> |
| <span data-ttu-id="48e96-192">5</span><span class="sxs-lookup"><span data-stu-id="48e96-192">5</span></span> | <span data-ttu-id="48e96-193">O tipo de pacote de chaves de licença Serviços de Área de Trabalho Remota é uma licença aberta.</span><span class="sxs-lookup"><span data-stu-id="48e96-193">The Remote Desktop Services license key pack type is an open license.</span></span> |
| <span data-ttu-id="48e96-194">6</span><span class="sxs-lookup"><span data-stu-id="48e96-194">6</span></span> | <span data-ttu-id="48e96-195">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="48e96-195">Not supported.</span></span> |

<span data-ttu-id="48e96-196">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="48e96-196">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-197">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48e96-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-199">Tipo de produto do Serviços de Área de Trabalho Remota pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="48e96-199">Product type of the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="48e96-200">Valor</span><span class="sxs-lookup"><span data-stu-id="48e96-200">Value</span></span> | <span data-ttu-id="48e96-201">Descrição</span><span class="sxs-lookup"><span data-stu-id="48e96-201">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="48e96-202">0</span><span class="sxs-lookup"><span data-stu-id="48e96-202">0</span></span> | <span data-ttu-id="48e96-203">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48e96-203">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="48e96-204">Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="48e96-204">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="48e96-205">1</span><span class="sxs-lookup"><span data-stu-id="48e96-205">1</span></span> | <span data-ttu-id="48e96-206">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário.</span><span class="sxs-lookup"><span data-stu-id="48e96-206">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="48e96-207">Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="48e96-207">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="48e96-208">2</span><span class="sxs-lookup"><span data-stu-id="48e96-208">2</span></span> | <span data-ttu-id="48e96-209">Este tipo de produto não é válido.</span><span class="sxs-lookup"><span data-stu-id="48e96-209">This product type is not valid.</span></span> |

<span data-ttu-id="48e96-210">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="48e96-210">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48e96-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-213">Versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-213">Product version for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="48e96-214">Valor</span><span class="sxs-lookup"><span data-stu-id="48e96-214">Value</span></span> | <span data-ttu-id="48e96-215">Descrição</span><span class="sxs-lookup"><span data-stu-id="48e96-215">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="48e96-216">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="48e96-216">"Windows Server 2012"</span></span> | <span data-ttu-id="48e96-217">Somente os servidores que executam o Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="48e96-217">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="48e96-218">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="48e96-218">"Windows Server 7"</span></span> | <span data-ttu-id="48e96-219">Somente os servidores que executam o Windows Server 2008 R2 ou o Windows Server 2008 têm suporte com esta licença.</span><span class="sxs-lookup"><span data-stu-id="48e96-219">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="48e96-220">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="48e96-220">"Windows Server 2008"</span></span> | <span data-ttu-id="48e96-221">Somente os servidores que executam o Windows Server 2008 têm suporte neste pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="48e96-221">Only servers running Windows Server 2008 are supported by this key pack.</span></span> |

<span data-ttu-id="48e96-222">**ProductVersionid**</span><span class="sxs-lookup"><span data-stu-id="48e96-222">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-223">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48e96-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-225">Identificador de versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-225">Product version identifier for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="48e96-226">Valor</span><span class="sxs-lookup"><span data-stu-id="48e96-226">Value</span></span> | <span data-ttu-id="48e96-227">Descrição</span><span class="sxs-lookup"><span data-stu-id="48e96-227">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="48e96-228">0</span><span class="sxs-lookup"><span data-stu-id="48e96-228">0</span></span> | <span data-ttu-id="48e96-229">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="48e96-229">Not supported</span></span> |
| <span data-ttu-id="48e96-230">1</span><span class="sxs-lookup"><span data-stu-id="48e96-230">1</span></span> | <span data-ttu-id="48e96-231">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="48e96-231">Not supported</span></span> |
| <span data-ttu-id="48e96-232">2</span><span class="sxs-lookup"><span data-stu-id="48e96-232">2</span></span> | <span data-ttu-id="48e96-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48e96-233">Windows Server 2008</span></span> |
| <span data-ttu-id="48e96-234">3</span><span class="sxs-lookup"><span data-stu-id="48e96-234">3</span></span> | <span data-ttu-id="48e96-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48e96-235">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="48e96-236">4</span><span class="sxs-lookup"><span data-stu-id="48e96-236">4</span></span> | <span data-ttu-id="48e96-237">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="48e96-237">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="48e96-238">5</span><span class="sxs-lookup"><span data-stu-id="48e96-238">5</span></span> | <span data-ttu-id="48e96-239">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="48e96-239">Windows Server 2016</span></span> |
| <span data-ttu-id="48e96-240">6</span><span class="sxs-lookup"><span data-stu-id="48e96-240">6</span></span> | <span data-ttu-id="48e96-241">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="48e96-241">Windows Server 2019</span></span> |

<span data-ttu-id="48e96-242">**TotalLicenses**</span><span class="sxs-lookup"><span data-stu-id="48e96-242">**TotalLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-243">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48e96-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-245">Número total de licenças no pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="48e96-245">Total number of licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="48e96-246">**TypeAndModel**</span><span class="sxs-lookup"><span data-stu-id="48e96-246">**TypeAndModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48e96-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="48e96-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48e96-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48e96-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48e96-249">Qualificador para tipo e modelo de pacote de chaves de Licenciamento TS.</span><span class="sxs-lookup"><span data-stu-id="48e96-249">Qualifier for TS Licensing key pack type and model.</span></span> <span data-ttu-id="48e96-250">Exemplos: licença de assinatura de VDI por dispositivo, TS CAL por usuário</span><span class="sxs-lookup"><span data-stu-id="48e96-250">Examples: VDI Per Device subscription license, TS Per User CAL</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48e96-251">Comentários</span><span class="sxs-lookup"><span data-stu-id="48e96-251">Remarks</span></span>

<span data-ttu-id="48e96-252">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="48e96-252">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="48e96-253">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="48e96-253">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="48e96-254">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="48e96-254">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="48e96-255">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="48e96-255">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="48e96-256">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="48e96-256">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="48e96-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48e96-257">Requirements</span></span>



| <span data-ttu-id="48e96-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="48e96-258">Requirement</span></span> | <span data-ttu-id="48e96-259">Valor</span><span class="sxs-lookup"><span data-stu-id="48e96-259">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e96-260">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48e96-260">Minimum supported client</span></span><br/> | <span data-ttu-id="48e96-261">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="48e96-261">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="48e96-262">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48e96-262">Minimum supported server</span></span><br/> | <span data-ttu-id="48e96-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48e96-263">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="48e96-264">Namespace</span><span class="sxs-lookup"><span data-stu-id="48e96-264">Namespace</span></span><br/>                | <span data-ttu-id="48e96-265">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="48e96-265">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="48e96-266">MOF</span><span class="sxs-lookup"><span data-stu-id="48e96-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48e96-267"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48e96-267"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="48e96-268">DLL</span><span class="sxs-lookup"><span data-stu-id="48e96-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e96-269"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48e96-269"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48e96-270">Confira também</span><span class="sxs-lookup"><span data-stu-id="48e96-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e96-271">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="48e96-271">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="48e96-272">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="48e96-272">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="48e96-273">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="48e96-273">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="48e96-274">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="48e96-274">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

