---
description: Fornece dados de configuração para um disco rígido virtual.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Msvm_VirtualHardDiskSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7f87ba072aaff03ab415ccabe803546a89192ecb1e28d85b628dd0655d47421
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068416"
---
# <a name="msvm_virtualharddisksettingdata-class"></a>Classe Msvm \_ VirtualHardDiskSettingData

Fornece dados de configuração para um disco rígido virtual.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ VirtualHardDiskSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ VirtualHardDiskSettingData** tem essas propriedades.

<dl> <dt>

**Blocksize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tamanho do bloco usado pelo disco rígido virtual, em bytes.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "Dados de Configuração de Disco Rígido Virtual".

</dd> <dt>

**DataAlignment**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica o alinhamento desejado, em bytes, para o payload de dados do disco virtual

> [!Note]  
> Adicionado na Windows 10, versão 1709.

 

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Configurando dados para um disco rígido virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Formato**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O formato do disco rígido virtual. Esse será um dos valores a seguir.

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span id="VHD"></span><span id="vhd"></span>**VHD** (2)


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)


</dt> <dd>

> [!Note]  
> Adicionado em Windows 10 e Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**IsPmemCompatible**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica se o disco virtual pode ser usado como o armazenamento de backup para um dispositivo de memória persistente.

> [!Note]  
> Adicionado na Windows 10, versão 1709.

 

</dd> <dt>

**LogicalSectorSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tamanho do setor lógico usado pelo disco rígido virtual, em bytes.

</dd> <dt>

**MaxInternalSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tamanho máximo do disco rígido virtual como exibivel pela máquina virtual, em bytes. Esse tamanho será arredondado para o próximo maior múltiplo do tamanho do setor.

</dd> <dt>

**ParentIdentifier**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O GUID usado para identificar exclusivamente o pai do disco rígido virtual. Se o disco rígido virtual não tiver um pai, esse campo será vazio.

> [!Note]  
> Adicionado em Windows 10 e Windows Server 2016.

 

</dd> <dt>

**ParentPath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O pai do disco rígido virtual. Se o disco rígido virtual não tiver um pai, essa propriedade será vazia.

</dd> <dt>

**ParentTimestamp**
</dt> <dd> <dl> <dt>

Tipo de dados: **DATETIME**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O timestamp do pai do disco rígido virtual. Se o disco rígido virtual não tiver um pai, esse campo será vazio.

> [!Note]  
> Adicionado em Windows 10 e Windows Server 2016.

 

</dd> <dt>

**Caminho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O caminho totalmente qualificado do disco rígido virtual.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tamanho do setor físico usado pelo disco rígido virtual, em bytes.

</dd> <dt>

**PmemAddressAbstractionType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O método de abstração de endereço de memória persistente a ser usado com esse disco virtual.

> [!Note]  
> Adicionado na Windows 10, versão 1709.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (0)


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

**BTT** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O tipo de disco rígido virtual. Esse será um dos valores a seguir.

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Corrigido** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

**Dinâmico** (3)


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

**Diferenciação** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualDiskId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O GUID usado para identificar exclusivamente o disco virtual.

Quando o método [**Msvm \_ ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) retorna uma instância de **Msvm \_ VirtualHardDiskSettingData**, o cliente pode usar essa propriedade para obter a ID de disco exclusiva do VHD.

Na detecção de conflitos ou de outra forma, um cliente pode definir o valor **virtualDiskId** como um novo GUID e passar essa instância **\_ de VirtualHardDiskSettingData** para o método [**Msvm \_ ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) para alterar a ID de disco do VHD. Se o VHD não for um VHDX ou se o VHD estiver anexado, a operação falhará. A operação também falhará se o valor passado estiver malformado, ou seja, não um GUID ou tiver todos os 0s. A operação terá êxito silenciosamente se o valor passado for o mesmo que a ID do disco atual.

Os erros gerados pela [**função SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) são gerados por meio dessa propriedade. Um cliente também pode usar o mesmo mecanismo para fornecer o valor **VirtualDiskId** na criação do VHD por meio do método [**Msvm \_ ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) no mesmo namespace. Isso pode ser usado para criar VHDs VHD1 ou VHD2.

**Windows 8.1:** Esse valor não tem suporte até que Windows 8.1 e Windows Server 2012 R2.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração \_ cimData**](cim-settingdata.md)
</dt> <dt>

[**GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

