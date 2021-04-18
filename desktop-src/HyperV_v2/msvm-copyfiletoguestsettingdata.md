---
description: Representa os parâmetros para copiar um arquivo do host para o convidado.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Classe Msvm_CopyFileToGuestSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810351"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a><span data-ttu-id="bedd3-103">\_Classe Msvm CopyFileToGuestSettingData</span><span class="sxs-lookup"><span data-stu-id="bedd3-103">Msvm\_CopyFileToGuestSettingData class</span></span>

<span data-ttu-id="bedd3-104">Representa os parâmetros para copiar um arquivo do host para o convidado.</span><span class="sxs-lookup"><span data-stu-id="bedd3-104">Represents the parameters for copying a file from the host into the guest.</span></span> <span data-ttu-id="bedd3-105">Essa classe deriva do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bedd3-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="bedd3-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bedd3-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bedd3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bedd3-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="bedd3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bedd3-108">Members</span></span>

<span data-ttu-id="bedd3-109">A classe **Msvm \_ CopyFileToGuestSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bedd3-109">The **Msvm\_CopyFileToGuestSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="bedd3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bedd3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bedd3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bedd3-111">Properties</span></span>

<span data-ttu-id="bedd3-112">A classe **Msvm \_ CopyFileToGuestSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bedd3-112">The **Msvm\_CopyFileToGuestSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bedd3-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="bedd3-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bedd3-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bedd3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bedd3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-116">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="bedd3-116">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="bedd3-117">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bedd3-117">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="bedd3-118">**Createfullpath**</span><span class="sxs-lookup"><span data-stu-id="bedd3-118">**CreateFullPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bedd3-119">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="bedd3-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bedd3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bedd3-121">Indica se os diretórios ausentes no caminho do arquivo de destino devem ser criados antes de copiar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="bedd3-121">Indicates whether missing directories in the destination file's path must be created before copying the file.</span></span>

</dd> <dt>

<span data-ttu-id="bedd3-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bedd3-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bedd3-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bedd3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bedd3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bedd3-125">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bedd3-125">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="bedd3-126">**DestinationPath**</span><span class="sxs-lookup"><span data-stu-id="bedd3-126">**DestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bedd3-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bedd3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bedd3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bedd3-129">O caminho completo do arquivo de destino a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="bedd3-129">The complete path of the destination file to be copied.</span></span> <span data-ttu-id="bedd3-130">Esse arquivo de destino deve ser acessível para o convidado e pode conter variáveis de ambiente, que são expandidas pelo convidado.</span><span class="sxs-lookup"><span data-stu-id="bedd3-130">This destination file must be accessible to the guest and can contain environment variables, which are expanded by the guest.</span></span> <span data-ttu-id="bedd3-131">Se o caminho especificado for um diretório existente no convidado, o arquivo de destino será criado nesse diretório.</span><span class="sxs-lookup"><span data-stu-id="bedd3-131">If the path specified is an existing directory in the guest, the destination file is created in this directory.</span></span> <span data-ttu-id="bedd3-132">Nesse caso, o nome do arquivo de **SourcePath** é usado como o nome do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="bedd3-132">In this case, the file name from **SourcePath** is used as the destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="bedd3-133">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bedd3-133">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bedd3-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bedd3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bedd3-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bedd3-136">O nome de exibição para esta instância de SettingData.</span><span class="sxs-lookup"><span data-stu-id="bedd3-136">The display name for this instance of SettingData.</span></span> <span data-ttu-id="bedd3-137">Além disso, o nome de exibição pode ser usado como uma propriedade de índice para uma pesquisa ou consulta.</span><span class="sxs-lookup"><span data-stu-id="bedd3-137">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="bedd3-138">(Observação: o nome não precisa ser exclusivo em um namespace.)</span><span class="sxs-lookup"><span data-stu-id="bedd3-138">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="bedd3-139">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bedd3-139">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bedd3-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bedd3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bedd3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-142">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="bedd3-142">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bedd3-143">Dentro do escopo do namespace de instanciação, a InstanceID identifica de forma opaca e exclusiva uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="bedd3-143">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bedd3-144">Para garantir a exclusividade no NameSpace, o valor de InstanceID deve ser construído usando o seguinte algoritmo "preferencial": *OrgID*:*LocalId* em que *OrgID* e *LocalId* são separados por dois-pontos (:) e onde *OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que está criando ou definindo a InstanceId ou que é uma ID registrada atribuída à entidade de negócios por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="bedd3-144">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="bedd3-145">(Esse requisito é semelhante ao *SchemaName* \_ Estrutura *ClassName* de nomes de classe de esquema.) Além disso, para garantir a exclusividade, *OrgID* não deve conter dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="bedd3-145">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="bedd3-146">Ao usar esse algoritmo, os primeiros dois-pontos para aparecer em InstanceID devem aparecer entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="bedd3-146">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="bedd3-147">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos subjacentes (reais) diferentes.</span><span class="sxs-lookup"><span data-stu-id="bedd3-147">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="bedd3-148">Se o algoritmo preferencial acima não for usado, a entidade de definição deverá garantir que a InstanceID resultante não seja reutilizada em quaisquer InstanceIDs produzidas por esse ou outros provedores para o NameSpace dessa instância.</span><span class="sxs-lookup"><span data-stu-id="bedd3-148">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="bedd3-149">Para instâncias definidas por DMTF, o algoritmo "preferencial" deve ser usado com o *OrgID* definido como CIM.</span><span class="sxs-lookup"><span data-stu-id="bedd3-149">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="bedd3-150">**OverwriteExisting**</span><span class="sxs-lookup"><span data-stu-id="bedd3-150">**OverwriteExisting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bedd3-151">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="bedd3-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bedd3-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bedd3-153">Indica se um arquivo de destino existente deve ser substituído.</span><span class="sxs-lookup"><span data-stu-id="bedd3-153">Indicates whether an existing destination file must be overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="bedd3-154">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="bedd3-154">**SourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bedd3-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bedd3-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bedd3-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bedd3-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bedd3-157">O caminho completo do arquivo de origem a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="bedd3-157">The complete path of the source file to be copied.</span></span> <span data-ttu-id="bedd3-158">Esse arquivo de origem deve ser acessível para o host Hyper-V e pode conter variáveis de ambiente, que são expandidas pelo host Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="bedd3-158">This source file must be accessible to the Hyper-V host and can contain environment variables, which are expanded by the Hyper-V host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bedd3-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bedd3-159">Requirements</span></span>



| <span data-ttu-id="bedd3-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="bedd3-160">Requirement</span></span> | <span data-ttu-id="bedd3-161">Valor</span><span class="sxs-lookup"><span data-stu-id="bedd3-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bedd3-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bedd3-162">Minimum supported client</span></span><br/> | <span data-ttu-id="bedd3-163">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bedd3-163">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bedd3-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bedd3-164">Minimum supported server</span></span><br/> | <span data-ttu-id="bedd3-165">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="bedd3-165">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bedd3-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="bedd3-166">Namespace</span></span><br/>                | <span data-ttu-id="bedd3-167">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bedd3-167">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bedd3-168">MOF</span><span class="sxs-lookup"><span data-stu-id="bedd3-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bedd3-169"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bedd3-169"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bedd3-170">DLL</span><span class="sxs-lookup"><span data-stu-id="bedd3-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bedd3-171"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bedd3-171"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bedd3-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="bedd3-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bedd3-173">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="bedd3-173">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="bedd3-174">[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bedd3-174">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

