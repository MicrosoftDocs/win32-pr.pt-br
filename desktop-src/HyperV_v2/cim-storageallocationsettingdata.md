---
description: Representa as configurações para a alocação do armazenamento virtual.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: Classe CIM_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662195"
---
# <a name="cim_storageallocationsettingdata-class"></a><span data-ttu-id="2517f-103">\_Classe CIM StorageAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="2517f-103">CIM\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="2517f-104">Representa as configurações para a alocação do armazenamento virtual.</span><span class="sxs-lookup"><span data-stu-id="2517f-104">Represents settings for the allocation of virtual storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="2517f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2517f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a><span data-ttu-id="2517f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2517f-106">Members</span></span>

<span data-ttu-id="2517f-107">A classe **CIM \_ StorageAllocationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2517f-107">The **CIM\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2517f-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2517f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2517f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2517f-109">Properties</span></span>

<span data-ttu-id="2517f-110">A classe **CIM \_ StorageAllocationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2517f-110">The **CIM\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2517f-111">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="2517f-111">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2517f-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-114">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Acesso**")</span><span class="sxs-lookup"><span data-stu-id="2517f-114">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**Access**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-115">O suporte de leitura/gravação da alocação de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2517f-115">The read/write support of the storage allocation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2517f-116">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2517f-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="2517f-117">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="2517f-117">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="2517f-118">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="2517f-118">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="2517f-119">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="2517f-119">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2517f-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2517f-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2517f-121">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="2517f-121">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2517f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-124">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="2517f-124">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-125">Um identificador exclusivo da extensão de armazenamento do host.</span><span class="sxs-lookup"><span data-stu-id="2517f-125">A unique identifier of the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="2517f-126">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="2517f-126">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2517f-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-129">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="2517f-129">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-130">O formato do valor da propriedade **HostExtentName** .</span><span class="sxs-lookup"><span data-stu-id="2517f-130">The format that of the **HostExtentName** property value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2517f-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2517f-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2517f-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="2517f-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="2517f-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="2517f-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2517f-134">O número de série/fornecedor/modelo (SNVM) SNVM é 3 cadeias de caracteres que representam o nome do fornecedor, o nome do produto dentro do namespace do fornecedor e o número de série no namespace do modelo.</span><span class="sxs-lookup"><span data-stu-id="2517f-134">Serial Number/Vendor/Model (SNVM) SNVM is 3 strings representing the vendor name, product name within the vendor namespace, and the serial number within the model namespace.</span></span> <span data-ttu-id="2517f-135">As cadeias de caracteres são delimitadas por um ' + '.</span><span class="sxs-lookup"><span data-stu-id="2517f-135">Strings are delimited with a '+'.</span></span> <span data-ttu-id="2517f-136">Os espaços podem ser incluídos e são significativos.</span><span class="sxs-lookup"><span data-stu-id="2517f-136">Spaces may be included and are significant.</span></span> <span data-ttu-id="2517f-137">O número de série é a representação de texto do número de série em maiúsculas hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="2517f-137">The serial number is the text representation of the serial number in hexadecimal upper case.</span></span> <span data-ttu-id="2517f-138">Isso representa o fornecedor e a ID do modelo de dados de consulta SCSI; o campo fornecedor deve ter 8 caracteres de largura e o campo produto deve ter 16 caracteres de largura.</span><span class="sxs-lookup"><span data-stu-id="2517f-138">This represents the vendor and model ID from SCSI Inquiry data; the vendor field MUST be 8 characters wide and the product field MUST be 16 characters wide.</span></span> <span data-ttu-id="2517f-139">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="2517f-139">For example,</span></span>

<span data-ttu-id="2517f-140">' Acme \_ \_ \_ \_ + super Disk \_ \_ \_ \_ \_ \_ + 124437458 ' ( \_ é um caractere de espaço)</span><span class="sxs-lookup"><span data-stu-id="2517f-140">'ACME\_\_\_\_+SUPER DISK\_\_\_\_\_\_+124437458' (\_ is a space character)</span></span>

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="2517f-141"><span id="NAA"></span><span id="naa"></span>**Naa** (9)</span><span class="sxs-lookup"><span data-stu-id="2517f-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>


</dt> <dd>

<span data-ttu-id="2517f-142">9 = NAA como um formato genérico.</span><span class="sxs-lookup"><span data-stu-id="2517f-142">9 = NAA as a generic format.</span></span> <span data-ttu-id="2517f-143">Consulte</span><span class="sxs-lookup"><span data-stu-id="2517f-143">See</span></span>

<span data-ttu-id="2517f-144"> https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span><span class="sxs-lookup"><span data-stu-id="2517f-144">https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span></span> <span data-ttu-id="2517f-145">Formatado como 16 ou 32 caracteres hexadecimais maiúsculos não separados (2 por byte binário).</span><span class="sxs-lookup"><span data-stu-id="2517f-145">Formatted as 16 or 32 unseparated uppercase hex characters (2 per binary byte).</span></span>

<span data-ttu-id="2517f-146">Por exemplo, ' 21000020372D3C73 '</span><span class="sxs-lookup"><span data-stu-id="2517f-146">For example '21000020372D3C73'</span></span>

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="2517f-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="2517f-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>


</dt> <dd>

<span data-ttu-id="2517f-148">EUI como um formato genérico (EUI64) consulte</span><span class="sxs-lookup"><span data-stu-id="2517f-148">EUI as a generic format (EUI64) See</span></span>

<span data-ttu-id="2517f-149"> https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span><span class="sxs-lookup"><span data-stu-id="2517f-149">https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span></span>

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="2517f-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="2517f-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>


</dt> <dd>

<span data-ttu-id="2517f-151">T10 formato do identificador do fornecedor como retornado pela consulta SCSI página VPD 83, identificador tipo 1.</span><span class="sxs-lookup"><span data-stu-id="2517f-151">T10 vendor identifier format as returned by SCSI Inquiry VPD page 83, identifier type 1.</span></span> <span data-ttu-id="2517f-152">Consulte especificação T10 SPC-3.</span><span class="sxs-lookup"><span data-stu-id="2517f-152">See T10 SPC-3 specification.</span></span> <span data-ttu-id="2517f-153">Esta é a ID do fornecedor ASCII de 8 bytes do registro T10 seguido por um identificador ASCII específico do fornecedor; os espaços são permitidos.</span><span class="sxs-lookup"><span data-stu-id="2517f-153">This is the 8-byte ASCII vendor ID from the T10 registry followed by a vendor specific ASCII identifier; spaces are permitted.</span></span> <span data-ttu-id="2517f-154">Para volumes não SCSI, ' SNVM ' pode ser a opção mais apropriada.</span><span class="sxs-lookup"><span data-stu-id="2517f-154">For non SCSI volumes, 'SNVM' may be the most appropriate choice.</span></span>

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="2517f-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nome do dispositivo do so** (12)</span><span class="sxs-lookup"><span data-stu-id="2517f-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>


</dt> <dd>

<span data-ttu-id="2517f-156">Nome do dispositivo do so (para LogicalDisks).</span><span class="sxs-lookup"><span data-stu-id="2517f-156">OS Device Name (for LogicalDisks).</span></span> <span data-ttu-id="2517f-157">Consulte Descrição do nome do LogicalDisk para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="2517f-157">See LogicalDisk Name description for details.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2517f-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2517f-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2517f-159">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="2517f-159">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-160">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2517f-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-162">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Namespace**")</span><span class="sxs-lookup"><span data-stu-id="2517f-162">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Namespace**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-163">O formato de nomenclatura para a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="2517f-163">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2517f-164">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2517f-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2517f-165">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="2517f-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="2517f-166">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="2517f-166">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="2517f-167">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="2517f-167">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="2517f-168">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="2517f-168">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="2517f-169">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="2517f-169">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="2517f-170">**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="2517f-170">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="2517f-171">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="2517f-171">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="2517f-172">**Namespace de dispositivo do so** (8)</span><span class="sxs-lookup"><span data-stu-id="2517f-172">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2517f-173">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2517f-173">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2517f-174">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="2517f-174">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-175">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2517f-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-177">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**","[**\_ baseado em CIM**](cim-basedon.md).**StartingAddress**")</span><span class="sxs-lookup"><span data-stu-id="2517f-177">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**", "[**CIM\_BasedOn**](cim-basedon.md).**StartingAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-178">O endereço inicial na extensão de armazenamento do host.</span><span class="sxs-lookup"><span data-stu-id="2517f-178">The starting address on the host storage extent.</span></span> <span data-ttu-id="2517f-179">Um Val nulo; UE indica que não há mapeamento direto entre a extensão de armazenamento virtual e a extensão de armazenamento do host.</span><span class="sxs-lookup"><span data-stu-id="2517f-179">A NULL val;ue indicates that there is no direct mapping between the virtual storage extent and the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="2517f-180">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2517f-180">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-181">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2517f-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-183">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="2517f-183">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-184">O tamanho, em bytes, dos blocos que são alocados no host para a alocação de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2517f-184">The size, in bytes, of the blocks that are allocated on the host for the storage allocation.</span></span> <span data-ttu-id="2517f-185">Se o tamanho do bloco for variável, o tamanho máximo do bloco em bytes deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="2517f-185">If the block size is variable, then the maximum block size in bytes should be specified.</span></span> <span data-ttu-id="2517f-186">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não se aplicar, o valor "1" (desconhecido) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="2517f-186">If the block size is unknown or if a block concept does not apply, then the value "1" (unknown) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="2517f-187">**Limite**</span><span class="sxs-lookup"><span data-stu-id="2517f-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-188">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2517f-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-190">Qualificadores: [**substituem**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (**" \_ CIM StorageAllocationSettingData**.**HostResourceBlockSize**")</span><span class="sxs-lookup"><span data-stu-id="2517f-190">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-191">A quantidade máxima de blocos que será concedida para a alocação de recursos de armazenamento no host.</span><span class="sxs-lookup"><span data-stu-id="2517f-191">The maximum amount of blocks that will be granted for the storage resource allocation on the host.</span></span> <span data-ttu-id="2517f-192">O tamanho do bloco é especificado pela propriedade **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="2517f-192">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="2517f-193">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="2517f-193">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2517f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-196">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="2517f-196">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-197">O formato da propriedade **HostExtentName** se a propriedade for definida como "1" (outra).</span><span class="sxs-lookup"><span data-stu-id="2517f-197">The format of the **HostExtentName** property if the property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="2517f-198">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="2517f-198">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2517f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-201">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="2517f-201">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-202">Uma cadeia de caracteres que descreve o namespace da propriedade **HostExtentName** se o valor da propriedade **HostExtentNameNamespace** for "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="2517f-202">A string that describes the namespace of the **HostExtentName** property if the value of the **HostExtentNameNamespace** property is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="2517f-203">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="2517f-203">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-204">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2517f-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-206">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("reserva"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")</span><span class="sxs-lookup"><span data-stu-id="2517f-206">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-207">A quantidade de blocos que têm garantia de disponibilidade para a alocação de recursos de armazenamento no host.</span><span class="sxs-lookup"><span data-stu-id="2517f-207">The amount of blocks that are guaranteed to be available for the storage resource allocation on the host.</span></span> <span data-ttu-id="2517f-208">O tamanho do bloco é especificado pela propriedade **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="2517f-208">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="2517f-209">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="2517f-209">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-210">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2517f-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-212">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**NumberOfBlocks**","**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**")</span><span class="sxs-lookup"><span data-stu-id="2517f-212">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM\_StorageAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-213">O número de blocos que a alocação de armazenamento apresenta ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="2517f-213">The number of blocks that the storage allocation presents to the consumer.</span></span>

> [!Note]  
> <span data-ttu-id="2517f-214">A propriedade **VirtualQuantity** pode especificar um tamanho de bloco de "1", mesmo se **VirtualResourceBlockSize** for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2517f-214">The **VirtualQuantity** property can specify a block size of "1", even if **VirtualResourceBlockSize** is unknown.</span></span>

 

</dd> <dt>

<span data-ttu-id="2517f-215">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="2517f-215">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2517f-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-218">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="2517f-218">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="2517f-219">As unidades usadas pela propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="2517f-219">The units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="2517f-220">Esse valor deverá ser definido como "Count (bloco de tamanho fixo)" ou "byte".</span><span class="sxs-lookup"><span data-stu-id="2517f-220">This value shall should be set to "count(fixed size block)" or "byte".</span></span> <span data-ttu-id="2517f-221">O valor padrão, "Count (bloco de tamanho fixo)", deve ser usado para um tamanho de bloco fixo e "byte" deve ser usado para um tamanho de bloco desconhecido ou variável.</span><span class="sxs-lookup"><span data-stu-id="2517f-221">The default value, "count(fixed size block)" should be used for a fixed block size, and "byte" should be used for an unknown or variable block size.</span></span>

</dd> <dt>

<span data-ttu-id="2517f-222">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="2517f-222">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2517f-223">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2517f-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2517f-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2517f-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2517f-225">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="2517f-225">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="2517f-226">O tamanho, em bytes, dos blocos que formam a solicitação de alocação de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2517f-226">The size, in bytes, of the blocks that form the storage allocation request.</span></span> <span data-ttu-id="2517f-227">Se o tamanho do bloco for variável, o tamanho máximo do bloco deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="2517f-227">If the block size is variable, then the maximum block size should be specified.</span></span> <span data-ttu-id="2517f-228">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não se aplicar, o tamanho do bloco deverá ser "1" (desconhecido).</span><span class="sxs-lookup"><span data-stu-id="2517f-228">If the block size is unknown or if a block concept does not apply, then the block size should be "1" (unknown).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2517f-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2517f-229">Requirements</span></span>



| <span data-ttu-id="2517f-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="2517f-230">Requirement</span></span> | <span data-ttu-id="2517f-231">Valor</span><span class="sxs-lookup"><span data-stu-id="2517f-231">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2517f-232">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2517f-232">Minimum supported client</span></span><br/> | <span data-ttu-id="2517f-233">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2517f-233">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2517f-234">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2517f-234">Minimum supported server</span></span><br/> | <span data-ttu-id="2517f-235">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2517f-235">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2517f-236">Namespace</span><span class="sxs-lookup"><span data-stu-id="2517f-236">Namespace</span></span><br/>                | <span data-ttu-id="2517f-237">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2517f-237">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2517f-238">MOF</span><span class="sxs-lookup"><span data-stu-id="2517f-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2517f-239"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2517f-239"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2517f-240">DLL</span><span class="sxs-lookup"><span data-stu-id="2517f-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2517f-241"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2517f-241"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2517f-242">Confira também</span><span class="sxs-lookup"><span data-stu-id="2517f-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2517f-243">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="2517f-243">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

