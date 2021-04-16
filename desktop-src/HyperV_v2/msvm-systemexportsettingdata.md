---
description: Associa uma máquina virtual e seus dados de configuração de exportação.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Classe Msvm_SystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752472"
---
# <a name="msvm_systemexportsettingdata-class"></a>\_Classe Msvm SystemExportSettingData

Associa uma máquina virtual e seus dados de configuração de exportação. Antes de chamar o método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) , uma instância de [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) pode ser recuperada usando essa associação.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SystemExportSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ SystemExportSettingData** tem essas propriedades.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração referenciada está sendo usada no momento na operação do elemento ou se essas informações são desconhecidas. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valor                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Current<br/>     |
| <dl> <dt>2</dt> </dl> | Não atual<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração referenciada é uma configuração padrão para o elemento ou se essas informações são desconhecidas. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valor                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Padrão<br/>     |
| <dl> <dt>2</dt> </dl> | Não padrão<br/> |



 

</dd> <dt>

**Isnext**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração referenciada é a próxima configuração a ser aplicada. Por exemplo, o aplicativo pode ocorrer em uma solicitação de reinicialização, redefinição e reconfiguração. Essa pode ser uma configuração permanente ou uma configuração usada apenas uma vez, conforme indicado pelo sinalizador. Se for uma configuração permanente, a configuração será aplicada toda vez que o elemento gerenciado for reinicializado, até que esse sinalizador seja redefinido manualmente. No entanto, se for um uso único, o sinalizador será limpo automaticamente depois que as configurações forem aplicadas. Além disso, se esse sinalizador for especificado (ou seja, definido com um valor diferente de 0 (desconhecido)), isso terá precedência sobre quaisquer dados de configuração que possam ter sido especificados como padrão. Por exemplo: se o elemento gerenciado for um sistema de computador e o valor desse sinalizador for 1 (próximo), a configuração entrará em vigor na próxima vez que o sistema for redefinido. E, a menos que esse sinalizador seja alterado, ele será mantido para redefinições subsequentes do sistema. No entanto, se esse sinalizador for definido como 3 (é próximo para uso único), essa configuração será usada apenas uma vez e o sinalizador será redefinido depois de 2 (não está próximo). Portanto, no exemplo acima, se o sistema reinicializar em uma rápida sucessão, a configuração não será usada na segunda reinicialização.

Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valor                                                                        | Significado                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>                |
| <dl> <dt>1</dt> </dl> | É o próximo<br/>                |
| <dl> <dt>2</dt> </dl> | Não é o próximo<br/>            |
| <dl> <dt>3</dt> </dl> | É o próximo para uso único<br/> |



 

</dd> <dt>

**Managedelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ sistema de ComputerSystem CIM**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. managedelement")
</dt> </dl>

Referência à máquina virtual. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. SettingData")
</dt> </dl>

Referência aos dados de configuração de exportação para a máquina virtual. Essa propriedade é herdada do [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ SystemExportSettingData** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

