---
description: Representa os parâmetros para definir a origem de inicialização de uma máquina virtual.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Classe Msvm_BootSourceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782813"
---
# <a name="msvm_bootsourcesettingdata-class"></a><span data-ttu-id="9df22-103">\_Classe Msvm BootSourceSettingData</span><span class="sxs-lookup"><span data-stu-id="9df22-103">Msvm\_BootSourceSettingData class</span></span>

<span data-ttu-id="9df22-104">Representa os parâmetros para definir a origem de inicialização de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9df22-104">Represents the parameters to set the boot source of a virtual machine.</span></span> <span data-ttu-id="9df22-105">Essa classe deriva do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9df22-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="9df22-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9df22-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df22-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9df22-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a><span data-ttu-id="9df22-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9df22-108">Members</span></span>

<span data-ttu-id="9df22-109">A classe **Msvm \_ BootSourceSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9df22-109">The **Msvm\_BootSourceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9df22-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9df22-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9df22-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9df22-111">Properties</span></span>

<span data-ttu-id="9df22-112">A classe **Msvm \_ BootSourceSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9df22-112">The **Msvm\_BootSourceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9df22-113">**BootSourceDescription**</span><span class="sxs-lookup"><span data-stu-id="9df22-113">**BootSourceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df22-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df22-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df22-116">A descrição da fonte de inicialização fornecida pelo firmware.</span><span class="sxs-lookup"><span data-stu-id="9df22-116">The description of the boot source provided by the firmware.</span></span>

</dd> <dt>

<span data-ttu-id="9df22-117">**BootSourceType**</span><span class="sxs-lookup"><span data-stu-id="9df22-117">**BootSourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9df22-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9df22-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df22-120">Um valor de enumeração que especifica o tipo da origem de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9df22-120">An enumeration value that specifies the type of the boot source.</span></span>

<span data-ttu-id="9df22-121">Estes são os valores válidos:</span><span class="sxs-lookup"><span data-stu-id="9df22-121">These are valid values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9df22-122">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9df22-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

<span data-ttu-id="9df22-123">**Unidade** (1)</span><span class="sxs-lookup"><span data-stu-id="9df22-123">**Drive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="9df22-124">**Rede** (2)</span><span class="sxs-lookup"><span data-stu-id="9df22-124">**Network** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

<span data-ttu-id="9df22-125">**Arquivo** (3)</span><span class="sxs-lookup"><span data-stu-id="9df22-125">**File** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9df22-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9df22-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df22-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df22-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df22-129">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="9df22-129">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="9df22-130">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9df22-130">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="9df22-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9df22-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df22-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df22-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df22-134">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9df22-134">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="9df22-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9df22-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df22-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df22-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df22-138">O nome de exibição para esta instância de SettingData.</span><span class="sxs-lookup"><span data-stu-id="9df22-138">The display name for this instance of SettingData.</span></span> <span data-ttu-id="9df22-139">Além disso, o nome de exibição pode ser usado como uma propriedade de índice para uma pesquisa ou consulta.</span><span class="sxs-lookup"><span data-stu-id="9df22-139">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="9df22-140">(Observação: o nome não precisa ser exclusivo em um namespace.)</span><span class="sxs-lookup"><span data-stu-id="9df22-140">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="9df22-141">**FirmwareDevicePath**</span><span class="sxs-lookup"><span data-stu-id="9df22-141">**FirmwareDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df22-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df22-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df22-144">O caminho nativo que o firmware usa para descrever o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9df22-144">The native path that the firmware uses to describe the device.</span></span>

</dd> <dt>

<span data-ttu-id="9df22-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9df22-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df22-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df22-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df22-148">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="9df22-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9df22-149">Dentro do escopo do namespace de instanciação, a InstanceID identifica de forma opaca e exclusiva uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="9df22-149">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9df22-150">Para garantir a exclusividade no NameSpace, o valor de InstanceID deve ser construído usando o seguinte algoritmo "preferencial": *OrgID*:*LocalId* em que *OrgID* e *LocalId* são separados por dois-pontos (:) e onde *OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que está criando ou definindo a InstanceId ou que é uma ID registrada atribuída à entidade de negócios por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="9df22-150">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="9df22-151">(Esse requisito é semelhante ao *SchemaName* \_ Estrutura *ClassName* de nomes de classe de esquema.) Além disso, para garantir a exclusividade, *OrgID* não deve conter dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="9df22-151">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="9df22-152">Ao usar esse algoritmo, os primeiros dois-pontos para aparecer em InstanceID devem aparecer entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="9df22-152">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="9df22-153">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos subjacentes (reais) diferentes.</span><span class="sxs-lookup"><span data-stu-id="9df22-153">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="9df22-154">Se o algoritmo preferencial acima não for usado, a entidade de definição deverá garantir que a InstanceID resultante não seja reutilizada em quaisquer InstanceIDs produzidas por esse ou outros provedores para o NameSpace dessa instância.</span><span class="sxs-lookup"><span data-stu-id="9df22-154">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="9df22-155">Para instâncias definidas por DMTF, o algoritmo "preferencial" deve ser usado com o *OrgID* definido como CIM.</span><span class="sxs-lookup"><span data-stu-id="9df22-155">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="9df22-156">**OptionalData**</span><span class="sxs-lookup"><span data-stu-id="9df22-156">**OptionalData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-157">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="9df22-157">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9df22-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9df22-159">Qualificadores: **octetstring**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="9df22-159">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9df22-160">Dados opcionais fornecidos pelo firmware.</span><span class="sxs-lookup"><span data-stu-id="9df22-160">Optional data provided by the firmware.</span></span>

> [!Note]  
> <span data-ttu-id="9df22-161">Propriedade adicionada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9df22-161">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="9df22-162">**OtherLocation**</span><span class="sxs-lookup"><span data-stu-id="9df22-162">**OtherLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9df22-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9df22-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9df22-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9df22-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9df22-165">As outras informações de local, se houver alguma, que o firmware usa para identificar a origem de inicialização com mais exclusividade.</span><span class="sxs-lookup"><span data-stu-id="9df22-165">The other location info, if any, that the firmware uses to further uniquely identify the boot source.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9df22-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9df22-166">Requirements</span></span>



| <span data-ttu-id="9df22-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="9df22-167">Requirement</span></span> | <span data-ttu-id="9df22-168">Valor</span><span class="sxs-lookup"><span data-stu-id="9df22-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9df22-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9df22-169">Minimum supported client</span></span><br/> | <span data-ttu-id="9df22-170">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9df22-170">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9df22-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9df22-171">Minimum supported server</span></span><br/> | <span data-ttu-id="9df22-172">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="9df22-172">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9df22-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="9df22-173">Namespace</span></span><br/>                | <span data-ttu-id="9df22-174">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9df22-174">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9df22-175">MOF</span><span class="sxs-lookup"><span data-stu-id="9df22-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9df22-176"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9df22-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9df22-177">DLL</span><span class="sxs-lookup"><span data-stu-id="9df22-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9df22-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9df22-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9df22-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="9df22-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df22-180">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="9df22-180">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="9df22-181">[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9df22-181">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 

