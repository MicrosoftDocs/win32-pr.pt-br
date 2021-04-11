---
description: A \_ classe WMI OnBoardDevice do Win32 representa dispositivos de adaptador comuns incorporados à placa-mãe (placa do sistema).
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Classe Win32_OnBoardDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fae5416a4b3cbeda0d8c63f6834c0406e628013
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164148"
---
# <a name="win32_onboarddevice-class"></a><span data-ttu-id="81647-103">\_Classe Win32 OnBoardDevice</span><span class="sxs-lookup"><span data-stu-id="81647-103">Win32\_OnBoardDevice class</span></span>

<span data-ttu-id="81647-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OnBoardDevice do Win32** representa dispositivos de adaptador comuns incorporados à placa-mãe (placa do sistema).</span><span class="sxs-lookup"><span data-stu-id="81647-104">The **Win32\_OnBoardDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents common adapter devices built into the motherboard (system board).</span></span>

<span data-ttu-id="81647-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="81647-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="81647-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="81647-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81647-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81647-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="81647-108">Membros</span><span class="sxs-lookup"><span data-stu-id="81647-108">Members</span></span>

<span data-ttu-id="81647-109">A classe **Win32 \_ OnBoardDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="81647-109">The **Win32\_OnBoardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="81647-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81647-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81647-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81647-111">Properties</span></span>

<span data-ttu-id="81647-112">A classe **Win32 \_ OnBoardDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="81647-112">The **Win32\_OnBoardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81647-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="81647-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-116">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="81647-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="81647-117">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="81647-117">Short description of the object.</span></span>

<span data-ttu-id="81647-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81647-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-122">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="81647-122">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="81647-123">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="81647-123">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="81647-124">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="81647-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="81647-125">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-125">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="81647-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-129">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Descrição"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Descrição do SMBIOS \| tipo 10 \| ")</span><span class="sxs-lookup"><span data-stu-id="81647-129">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="81647-130">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="81647-130">Description of the object.</span></span>

<span data-ttu-id="81647-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-132">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="81647-132">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81647-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81647-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-135">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de dispositivo SMBIOS tipo 10 \| ")</span><span class="sxs-lookup"><span data-stu-id="81647-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Type n")</span></span>
</dt> </dl>

<span data-ttu-id="81647-136">Tipo de dispositivo que está sendo representado.</span><span class="sxs-lookup"><span data-stu-id="81647-136">Type of device being represented.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81647-137">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="81647-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81647-138">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="81647-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="81647-139">**Vídeo** (3)</span><span class="sxs-lookup"><span data-stu-id="81647-139">**Video** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

<span data-ttu-id="81647-140">**Controlador SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="81647-140">**SCSI Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="81647-141">**Ethernet** (5)</span><span class="sxs-lookup"><span data-stu-id="81647-141">**Ethernet** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="81647-142">**Token ring** (6)</span><span class="sxs-lookup"><span data-stu-id="81647-142">**Token Ring** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

<span data-ttu-id="81647-143">**Som** (7)</span><span class="sxs-lookup"><span data-stu-id="81647-143">**Sound** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81647-144">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="81647-144">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81647-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81647-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-147">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 10 \| status do dispositivo n")</span><span class="sxs-lookup"><span data-stu-id="81647-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Status n")</span></span>
</dt> </dl>

<span data-ttu-id="81647-148">Se for **true**, o dispositivo integrado estará disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="81647-148">If **TRUE**, the on-board device is available for use.</span></span>

</dd> <dt>

<span data-ttu-id="81647-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="81647-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-150">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81647-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81647-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81647-152">Se for **true**, um pacote físico poderá ser trocado de maneira intercambiável (se for possível substituir o elemento por um fisicamente diferente, mas equivalente um, enquanto o pacote recipiente tiver energia aplicada a ele).</span><span class="sxs-lookup"><span data-stu-id="81647-152">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="81647-153">Por exemplo, um pacote de unidade de disco inserido usando conectores de SCA é removível e pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="81647-153">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="81647-154">Todos os pacotes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="81647-154">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="81647-155">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="81647-155">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81647-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-157">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81647-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81647-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-159">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="81647-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="81647-160">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="81647-160">Date and time the object was installed.</span></span> <span data-ttu-id="81647-161">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="81647-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="81647-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-163">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="81647-163">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-166">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="81647-166">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="81647-167">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="81647-167">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="81647-168">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-168">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-169">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="81647-169">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-172">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="81647-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="81647-173">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="81647-173">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="81647-174">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-175">**Nome**</span><span class="sxs-lookup"><span data-stu-id="81647-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-178">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="81647-178">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="81647-179">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="81647-179">Label by which the object is known.</span></span> <span data-ttu-id="81647-180">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="81647-180">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="81647-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-182">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="81647-182">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81647-185">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="81647-185">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="81647-186">Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="81647-186">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="81647-187">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo ou puderem ser usados como uma chave de elemento, essa propriedade será **NULL** e os dados de código de barras serão usados como a chave de classe na propriedade de marca.</span><span class="sxs-lookup"><span data-stu-id="81647-187">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="81647-188">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-188">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-189">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="81647-189">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-192">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="81647-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="81647-193">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="81647-193">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="81647-194">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-195">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="81647-195">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-196">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81647-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81647-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81647-198">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="81647-198">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="81647-199">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-199">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-200">**Removível**</span><span class="sxs-lookup"><span data-stu-id="81647-200">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-201">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81647-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81647-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81647-203">Se for **true**, um pacote físico será removível (se for projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem encontrar a função do empacotamento geral).</span><span class="sxs-lookup"><span data-stu-id="81647-203">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="81647-204">Um pacote ainda poderá ser removível se a energia precisar ser "desativada" para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="81647-204">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="81647-205">Se a energia puder ser "ativada" e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="81647-205">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="81647-206">Por exemplo, uma bateria extra em um laptop é removível, assim como um pacote de unidade de disco inserido usando conectores SCA.</span><span class="sxs-lookup"><span data-stu-id="81647-206">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="81647-207">No entanto, o último pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="81647-207">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="81647-208">A tela de um laptop não é removível, nem uma fonte de alimentação não redundante.</span><span class="sxs-lookup"><span data-stu-id="81647-208">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="81647-209">A remoção desses componentes afetaria a função do empacotamento geral ou é impossível devido à forte integração do pacote.</span><span class="sxs-lookup"><span data-stu-id="81647-209">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="81647-210">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="81647-210">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-211">**Peças**</span><span class="sxs-lookup"><span data-stu-id="81647-211">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-212">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81647-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81647-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81647-214">Se for **true**, um pacote físico será substituível (se for possível substituir, FRU ou upgrade, o elemento com um fisicamente diferente).</span><span class="sxs-lookup"><span data-stu-id="81647-214">If **TRUE**, a physical package is replaceable (if it is possible to replace, FRU or upgrade, the element with a physically different one).</span></span> <span data-ttu-id="81647-215">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="81647-215">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="81647-216">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="81647-216">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="81647-217">Outro exemplo é um pacote de fornecimento de energia montado em trilhos deslizantes.</span><span class="sxs-lookup"><span data-stu-id="81647-217">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="81647-218">Todos os pacotes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="81647-218">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="81647-219">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="81647-219">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="81647-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-223">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="81647-223">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="81647-224">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="81647-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="81647-225">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="81647-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-229">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="81647-229">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="81647-230">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="81647-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="81647-231">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81647-232">**Status**</span><span class="sxs-lookup"><span data-stu-id="81647-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-235">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="81647-235">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="81647-236">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="81647-236">Current status of the object.</span></span> <span data-ttu-id="81647-237">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="81647-237">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="81647-238">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="81647-238">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="81647-239">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="81647-239">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="81647-240">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="81647-240">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="81647-241">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="81647-241">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="81647-242">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="81647-243">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="81647-243">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="81647-244">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="81647-244">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="81647-245">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="81647-245">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="81647-246">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="81647-246">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81647-247">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="81647-247">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="81647-248">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="81647-248">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="81647-249">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="81647-249">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="81647-250">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="81647-250">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="81647-251">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="81647-251">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="81647-252">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="81647-252">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="81647-253">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="81647-253">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="81647-254">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="81647-254">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="81647-255">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="81647-255">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81647-256">**Tag**</span><span class="sxs-lookup"><span data-stu-id="81647-256">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-259">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="81647-259">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="81647-260">Identificador exclusivo do dispositivo integrado conectado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="81647-260">Unique identifier of the on-board device connected to the system.</span></span>

<span data-ttu-id="81647-261">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="81647-262">Exemplo: "no dispositivo de placa 1"</span><span class="sxs-lookup"><span data-stu-id="81647-262">Example: "On Board Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="81647-263">**Versão**</span><span class="sxs-lookup"><span data-stu-id="81647-263">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81647-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81647-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81647-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81647-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81647-266">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="81647-266">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="81647-267">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="81647-267">Version of the physical element.</span></span>

<span data-ttu-id="81647-268">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="81647-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81647-269">Comentários</span><span class="sxs-lookup"><span data-stu-id="81647-269">Remarks</span></span>

<span data-ttu-id="81647-270">A classe **Win32 \_ OnBoardDevice** é derivada de [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="81647-270">The **Win32\_OnBoardDevice** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81647-271">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81647-271">Requirements</span></span>



| <span data-ttu-id="81647-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="81647-272">Requirement</span></span> | <span data-ttu-id="81647-273">Valor</span><span class="sxs-lookup"><span data-stu-id="81647-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81647-274">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81647-274">Minimum supported client</span></span><br/> | <span data-ttu-id="81647-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81647-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81647-276">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81647-276">Minimum supported server</span></span><br/> | <span data-ttu-id="81647-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81647-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81647-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="81647-278">Namespace</span></span><br/>                | <span data-ttu-id="81647-279">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="81647-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81647-280">MOF</span><span class="sxs-lookup"><span data-stu-id="81647-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81647-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81647-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81647-282">DLL</span><span class="sxs-lookup"><span data-stu-id="81647-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81647-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81647-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81647-284">Confira também</span><span class="sxs-lookup"><span data-stu-id="81647-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81647-285">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="81647-285">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dt>

[<span data-ttu-id="81647-286">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="81647-286">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
