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
ms.openlocfilehash: fe380b03daced6ca98a44c189c52b5842862aa2e033bf66a04f8dd1466968449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899666"
---
# <a name="cim_storageallocationsettingdata-class"></a>Classe CIM \_ StorageAllocationSettingData

Representa as configurações para a alocação do armazenamento virtual.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A **classe CIM \_ StorageAllocationSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ StorageAllocationSettingData** tem essas propriedades.

<dl> <dt>

**Acesso**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Acesso**")
</dt> </dl>

O suporte de leitura/gravação da alocação de armazenamento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Acessível** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Writeable** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Leitura/gravação com suporte** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**", "**Cim \_ StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM \_ StorageExtent**](cim-storageextent.md).**Nome**")
</dt> </dl>

Um identificador exclusivo da extensão de armazenamento do host.

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**", "**Cim \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**")
</dt> </dl>

O formato do valor da **propriedade HostExtentName.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)


</dt> <dd>

SNVM (Número de Série/Fornecedor/Modelo) SNVM são três cadeias de caracteres que representam o nome do fornecedor, o nome do produto no namespace do fornecedor e o número de série dentro do namespace do modelo. As cadeias de caracteres são delimitadas por um '+'. Os espaços podem ser incluídos e são significativos. O número de série é a representação de texto do número de série em letras maiúsculas hexadecimais. Isso representa o fornecedor e a ID do modelo dos dados de Consulta SCSI; O campo fornecedor DEVE ter 8 caracteres de largura e o campo do produto DEVE ter 16 caracteres de largura. Por exemplo,

'ACME \_ \_ \_ \_ +SUPER DISK \_ \_ \_ \_ \_ \_ +124437458' ( \_ é um caractere de espaço)

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span id="NAA"></span><span id="naa"></span>**NAA** (9)


</dt> <dd>

9 = NAA como um formato genérico. Consulte

https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html. Formatado como 16 ou 32 caracteres hexadados em maiúsculas não separados (2 por byte binário).

Por exemplo'21000020372D3C73'

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)


</dt> <dd>

EUI como um formato genérico (EUI64) Consulte

https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)


</dt> <dd>

Formato do identificador de fornecedor T10 conforme retornado pela VPD de Consulta SCSI página 83, tipo de identificador 1. Consulte Especificação do SPC-3 T10. Essa é a ID do fornecedor ASCII de 8 byte do registro T10 seguida por um identificador ASCII específico do fornecedor; espaços são permitidos. Para volumes não SCSI, 'SNVM' pode ser a opção mais apropriada.

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nome do dispositivo do** sistema operacional (12)


</dt> <dd>

Nome do dispositivo do sistema operacional (para LogicalDisks). Consulte LogicalDisk Name description para obter detalhes.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**", "**Cim \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM \_ StorageExtent**](cim-storageextent.md).**Namespace**")
</dt> </dl>

O formato de nomen por nome da **propriedade** Name.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

**VPD83Type3** (2)


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (3)


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (4)


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

**VPD80** (5)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Namespace do dispositivo do sistema** operacional (8)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**", "[**Cim \_ BasedOn**](cim-basedon.md).**StartingAddress**")
</dt> </dl>

O endereço inicial na extensão de armazenamento do host. Um valor NULL val;ue indica que não há mapeamento direto entre a extensão de armazenamento virtual e a extensão de armazenamento do host.

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")
</dt> </dl>

O tamanho, em bytes, dos blocos alocados no host para a alocação de armazenamento. Se o tamanho do bloco for variável, o tamanho máximo do bloco em bytes deverá ser especificado. Se o tamanho do bloco for desconhecido ou se um conceito de bloco não se aplicar, o valor "1" (desconhecido) deverá ser usado.

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](../wmisdk/standard-qualifiers.md) ("Limite"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**Cim \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

A quantidade máxima de blocos que serão concedidos para a alocação de recursos de armazenamento no host. O tamanho do bloco é especificado pela **propriedade HostResourceBlockSize.**

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")
</dt> </dl>

O formato da **propriedade HostExtentName** se a propriedade estiver definida como "1" (outro).

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")
</dt> </dl>

Uma cadeia de caracteres que descreve o namespace da propriedade **HostExtentName** se o valor da propriedade **HostExtentNameNamespace** for "1" (outro).

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("reserva"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

A quantidade de blocos que têm garantia de disponibilidade para a alocação de recursos de armazenamento no host. O tamanho do bloco é especificado pela propriedade **HostResourceBlockSize** .

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**NumberOfBlocks**","**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**")
</dt> </dl>

O número de blocos que a alocação de armazenamento apresenta ao consumidor.

> [!Note]  
> A propriedade **VirtualQuantity** pode especificar um tamanho de bloco de "1", mesmo se **VirtualResourceBlockSize** for desconhecido.

 

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**
</dt> </dl>

As unidades usadas pela propriedade **VirtualQuantity** . Esse valor deverá ser definido como "Count (bloco de tamanho fixo)" ou "byte". O valor padrão, "Count (bloco de tamanho fixo)", deve ser usado para um tamanho de bloco fixo e "byte" deve ser usado para um tamanho de bloco desconhecido ou variável.

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** (" byte ")
</dt> </dl>

O tamanho, em bytes, dos blocos que formam a solicitação de alocação de armazenamento. Se o tamanho do bloco for variável, o tamanho máximo do bloco deverá ser especificado. Se o tamanho do bloco for desconhecido ou se um conceito de bloco não se aplicar, o tamanho do bloco deverá ser "1" (desconhecido).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

