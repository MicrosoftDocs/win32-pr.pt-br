---
title: Classe MDM_WindowsLicensing
description: A \_ classe MDM WindowsLicensing foi projetada para cenários de gerenciamento relacionados ao licenciamento.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- Classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771688"
---
# <a name="mdm_windowslicensing-class"></a><span data-ttu-id="c5d03-105">\_Classe WindowsLicensing do MDM</span><span class="sxs-lookup"><span data-stu-id="c5d03-105">MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="c5d03-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c5d03-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c5d03-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c5d03-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c5d03-108">A classe **MDM \_ WindowsLicensing** foi projetada para cenários de gerenciamento relacionados ao licenciamento.</span><span class="sxs-lookup"><span data-stu-id="c5d03-108">The **MDM\_WindowsLicensing** class is designed for licensing related management scenarios.</span></span> <span data-ttu-id="c5d03-109">Atualmente, o escopo é limitado a atualizações de edição de dispositivos Windows 10 desktop e Mobile, como Windows 10 pro para Windows 10 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="c5d03-109">Currently the scope is limited to edition upgrades of Windows 10 desktop and mobile devices, such as Windows 10 Pro to Windows 10 Enterprise.</span></span> <span data-ttu-id="c5d03-110">Além disso, esse CSP fornece a capacidade de ativar ou alterar a chave do produto de dispositivos Windows 10 desktop.</span><span class="sxs-lookup"><span data-stu-id="c5d03-110">In addition, this CSP provides the capability to activate or change the product key of Windows 10 desktop devices.</span></span>

<span data-ttu-id="c5d03-111">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c5d03-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d03-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5d03-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a><span data-ttu-id="c5d03-113">Membros</span><span class="sxs-lookup"><span data-stu-id="c5d03-113">Members</span></span>

<span data-ttu-id="c5d03-114">A classe **MDM \_ WindowsLicensing** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c5d03-114">The **MDM\_WindowsLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="c5d03-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5d03-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="c5d03-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5d03-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c5d03-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5d03-117">Methods</span></span>

<span data-ttu-id="c5d03-118">A classe **MDM \_ WindowsLicensing** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c5d03-118">The **MDM\_WindowsLicensing** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c5d03-119">Método</span><span class="sxs-lookup"><span data-stu-id="c5d03-119">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c5d03-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5d03-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c5d03-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5d03-121"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c5d03-122">Instala uma chave do produto para dispositivos Windows 10 desktop.</span><span class="sxs-lookup"><span data-stu-id="c5d03-122">Installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="c5d03-123">Não reinicia.</span><span class="sxs-lookup"><span data-stu-id="c5d03-123">Does not reboot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c5d03-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5d03-124"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c5d03-125">Para verificar se a chave do produto (Product Key) inserida pode ser usada para uma atualização de edição, ativar ou alterar uma chave de produto do Windows 10 para dispositivos de desktop.</span><span class="sxs-lookup"><span data-stu-id="c5d03-125">Method to check if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c5d03-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5d03-126"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c5d03-127">Forneça uma licença para uma atualização de edição de dispositivos Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="c5d03-127">Provide a license for an edition upgrade of Windows 10 mobile devices.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c5d03-128">Esse processo de atualização não exige uma reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="c5d03-128">This upgrade process does not require a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="c5d03-129">O tipo de data é XML.</span><span class="sxs-lookup"><span data-stu-id="c5d03-129">The date type is XML.</span></span><br/> <span data-ttu-id="c5d03-130">A operação com suporte é executada.</span><span class="sxs-lookup"><span data-stu-id="c5d03-130">The supported operation is Execute.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="c5d03-131">O conteúdo do arquivo de licença XML deve ter um escape adequado (ou seja, não deve simplesmente ser um XML copiado), caso contrário, a atualização de edição em dispositivos Windows 10 Mobile falhará.</span><span class="sxs-lookup"><span data-stu-id="c5d03-131">The XML license file contents must be properly escaped (that is, it should not simply be a copied XML), otherwise the edition upgrade on Windows 10 mobile devices will fail.</span></span> <span data-ttu-id="c5d03-132">Para obter mais informações sobre a saída correta do arquivo de licença XML, consulte a seção 2,4 da <a href="https://www.w3.org/TR/xml/">especificação XML do W3C</a>. O arquivo de licença XML é adquirido do centro de serviços de licenciamento por volume da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5d03-132">For more information on proper escaping of the XML license file, see Section 2.4 of the <a href="https://www.w3.org/TR/xml/">W3C XML spec</a>. The XML license file is acquired from the Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="c5d03-133">Sua organização deve ter um contrato de licenciamento por volume com a Microsoft para acessar o Portal.</span><span class="sxs-lookup"><span data-stu-id="c5d03-133">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="c5d03-134">Estes são os caminhos de atualização de edição válidos ao usar este nó por meio de um pacote MDM ou de provisionamento:</span><span class="sxs-lookup"><span data-stu-id="c5d03-134">The following are valid edition upgrade paths when using this node through an MDM or provisioning package:</span></span>
<ul>
<li><span data-ttu-id="c5d03-135">Windows 10 Mobile para Windows 10 Mobile Enterprise</span><span class="sxs-lookup"><span data-stu-id="c5d03-135">Windows 10 Mobileto Windows 10 Mobile Enterprise</span></span><br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="c5d03-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5d03-136"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="c5d03-137">Dispara o dispositivo para pegar a chave do produto e atualizar a edição do cliente.</span><span class="sxs-lookup"><span data-stu-id="c5d03-137">Triggers the device to take the product key and upgrade the edition of the client.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c5d03-138">Esse processo de atualização requer uma reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="c5d03-138">This upgrade process requires a system restart.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="c5d03-139">A operação com suporte é executada.</span><span class="sxs-lookup"><span data-stu-id="c5d03-139">The supported operation is Execute.</span></span><br/> <span data-ttu-id="c5d03-140">Quando uma chave do produto é enviada por push de um servidor MDM para um dispositivo do usuário, o <strong>changepk.exe</strong> é executado usando a chave do produto.</span><span class="sxs-lookup"><span data-stu-id="c5d03-140">When a product key is pushed from an MDM server to a user's device, <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="c5d03-141">Após a conclusão, uma notificação é mostrada ao usuário de que uma nova edição do Windows 10 está disponível.</span><span class="sxs-lookup"><span data-stu-id="c5d03-141">After it completes, a notification is shown to the user that a new edition of Windows 10 is available.</span></span> <span data-ttu-id="c5d03-142">O usuário pode reiniciar o sistema manualmente ou, após duas horas, o dispositivo será reiniciado automaticamente para concluir a atualização.</span><span class="sxs-lookup"><span data-stu-id="c5d03-142">The user can then restart their system manually or, after two hours, the device will restart automatically to complete the upgrade.</span></span> <span data-ttu-id="c5d03-143">O usuário receberá uma notificação de lembrete 10 minutos antes da reinicialização automática.</span><span class="sxs-lookup"><span data-stu-id="c5d03-143">The user will receive a reminder notification 10 minutes before the automatic restart.</span></span><br/> <span data-ttu-id="c5d03-144">Depois que o dispositivo for reiniciado, o processo de upgrade de edição será reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c5d03-144">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="c5d03-145">O usuário receberá uma notificação de upgrade bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c5d03-145">The user will receive a notification of the successful upgrade.</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="c5d03-146">Se outra política exigir uma reinicialização do sistema que ocorra quando <strong>changepk.exe</strong> estiver em execução, a atualização da edição falhará.</span><span class="sxs-lookup"><span data-stu-id="c5d03-146">If another policy requires a system reboot that occurs when <strong>changepk.exe</strong> is running, the edition upgrade will fail.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="c5d03-147">Se uma chave do produto (Product Key) for inserida em um pacote de provisionamento e o usuário iniciar a instalação do pacote, uma notificação será mostrada ao usuário dizendo que o sistema será reiniciado para a conclusão da instalação do pacote.</span><span class="sxs-lookup"><span data-stu-id="c5d03-147">If a product key is entered in a provisioning package and the user begins installation of the package, a notification is shown to the user that their system will restart to complete the package installation.</span></span> <span data-ttu-id="c5d03-148">Após o consentimento explícito do usuário para continuar, o pacote continua a instalação e <strong>changepk.exe</strong> é executado usando a chave do produto.</span><span class="sxs-lookup"><span data-stu-id="c5d03-148">Upon explicit consent from the user to proceed, the package continues installation and <strong>changepk.exe</strong> runs using the product key.</span></span> <span data-ttu-id="c5d03-149">O usuário receberá uma notificação de lembrete 30 segundos antes do reinício automático.</span><span class="sxs-lookup"><span data-stu-id="c5d03-149">The user will receive a reminder notification 30 seconds before the automatic restart.</span></span> <br/> <span data-ttu-id="c5d03-150">Depois que o dispositivo for reiniciado, o processo de upgrade de edição será reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c5d03-150">After the device restarts, the edition upgrade process completes.</span></span> <span data-ttu-id="c5d03-151">O usuário receberá uma notificação de upgrade bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c5d03-151">The user will receive a notification of the successful upgrade.</span></span> <br/> <span data-ttu-id="c5d03-152">Esse nó também pode ser usado para ativar ou alterar uma chave do produto (Product Key) em uma edição específica do dispositivo de desktop do Windows 10 inserindo uma chave do produto (Product Key).</span><span class="sxs-lookup"><span data-stu-id="c5d03-152">This node can also be used to activate or change a product key on a particular edition of Windows 10 desktop device by entering a product key.</span></span> <span data-ttu-id="c5d03-153">A ativação ou a alteração de uma chave do produto não requer uma reinicialização e é um processo silencioso para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c5d03-153">Activation or changing a product key does not require a reboot and is a silent process for the user.</span></span><br/>
<blockquote>
[!Important]<br />
<span data-ttu-id="c5d03-154">A chave do produto (Product Key) inserida deve ter 29 caracteres (ou seja, deve incluir traços), caso contrário, a ativação, a atualização de edição ou a alteração da chave do produto em dispositivos com Windows 10 desktop falharão.</span><span class="sxs-lookup"><span data-stu-id="c5d03-154">The product key entered must be 29 characters (that is, it should include dashes), otherwise the activation, edition upgrade, or product key change on Windows 10 desktop devices will fail.</span></span> <span data-ttu-id="c5d03-155">A chave do produto é adquirida do centro de serviços de licenciamento por volume da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5d03-155">The product key is acquired from Microsoft Volume Licensing Service Center.</span></span> <span data-ttu-id="c5d03-156">Sua organização deve ter um contrato de licenciamento por volume com a Microsoft para acessar o Portal.</span><span class="sxs-lookup"><span data-stu-id="c5d03-156">Your organization must have a Volume Licensing contract with Microsoft to access the portal.</span></span>
</blockquote>
<br/> <span data-ttu-id="c5d03-157">Estes são os caminhos de atualização de edição válidos ao usar este nó por meio de um MDM:</span><span class="sxs-lookup"><span data-stu-id="c5d03-157">The following are valid edition upgrade paths when using this node through an MDM:</span></span>
<ul>
<li><span data-ttu-id="c5d03-158">Windows 10 Enterprise para Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="c5d03-158">Windows 10 Enterprise to Windows 10 Education</span></span></li>
<li><span data-ttu-id="c5d03-159">Windows 10 home to Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="c5d03-159">Windows 10 Home to Windows 10 Education</span></span></li>
<li><span data-ttu-id="c5d03-160">Windows 10 pro para Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="c5d03-160">Windows 10 Pro to Windows 10 Education</span></span></li>
<li><span data-ttu-id="c5d03-161">Windows 10 pro para Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="c5d03-161">Windows 10 Pro to Windows 10 Enterprise</span></span></li>
</ul>
<br/> <span data-ttu-id="c5d03-162">A ativação ou a alteração de uma chave do produto pode ser executada nas seguintes edições:</span><span class="sxs-lookup"><span data-stu-id="c5d03-162">Activation or changing a product key can be carried out on the following editions:</span></span>
<ul>
<li><span data-ttu-id="c5d03-163">Windows 10 Education</span><span class="sxs-lookup"><span data-stu-id="c5d03-163">Windows 10 Education</span></span></li>
<li><span data-ttu-id="c5d03-164">Windows 10 Enterprise</span><span class="sxs-lookup"><span data-stu-id="c5d03-164">Windows 10 Enterprise</span></span></li>
<li><span data-ttu-id="c5d03-165">Windows 10 Home</span><span class="sxs-lookup"><span data-stu-id="c5d03-165">Windows 10 Home</span></span></li>
<li><span data-ttu-id="c5d03-166">Windows 10 Pro</span><span class="sxs-lookup"><span data-stu-id="c5d03-166">Windows 10 Pro</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="c5d03-167">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5d03-167">Properties</span></span>

<span data-ttu-id="c5d03-168">A classe **MDM \_ WindowsLicensing** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c5d03-168">The **MDM\_WindowsLicensing** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c5d03-169">Edição</span><span class="sxs-lookup"><span data-stu-id="c5d03-169">Edition</span></span>](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5d03-170">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c5d03-170">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5d03-171">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c5d03-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c5d03-172">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c5d03-172">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5d03-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5d03-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5d03-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5d03-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5d03-175">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5d03-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5d03-176">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="c5d03-176">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="c5d03-177">LicenseKeyType</span><span class="sxs-lookup"><span data-stu-id="c5d03-177">LicenseKeyType</span></span>](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5d03-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5d03-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5d03-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c5d03-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c5d03-180">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c5d03-180">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5d03-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5d03-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5d03-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5d03-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5d03-183">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5d03-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5d03-184">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="c5d03-184">Describes the full path to the parent node.</span></span> <span data-ttu-id="c5d03-185">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="c5d03-185">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="c5d03-186">Status</span><span class="sxs-lookup"><span data-stu-id="c5d03-186">Status</span></span>](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5d03-187">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c5d03-187">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5d03-188">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c5d03-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5d03-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5d03-189">Requirements</span></span>



| <span data-ttu-id="c5d03-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5d03-190">Requirement</span></span> | <span data-ttu-id="c5d03-191">Valor</span><span class="sxs-lookup"><span data-stu-id="c5d03-191">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d03-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5d03-192">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d03-193">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c5d03-193">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5d03-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5d03-194">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d03-195">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c5d03-195">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c5d03-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5d03-196">Namespace</span></span><br/>                | <span data-ttu-id="c5d03-197">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c5d03-197">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c5d03-198">MOF</span><span class="sxs-lookup"><span data-stu-id="c5d03-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5d03-199"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5d03-199"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5d03-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c5d03-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5d03-201"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5d03-201"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d03-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5d03-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d03-203">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="c5d03-203">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

