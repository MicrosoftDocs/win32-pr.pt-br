---
description: Associa uma máquina virtual e seus dados de configuração de exportação.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData classe
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
ms.openlocfilehash: 39e096c466dd4accc1a2c87ececd6ce23ba27cb173e6b5fa0d6728852ad59cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811866"
---
# <a name="msvm_systemexportsettingdata-class"></a>Classe Msvm \_ SystemExportSettingData

Associa uma máquina virtual e seus dados de configuração de exportação. Antes de chamar o método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService,**](msvm-virtualsystemmanagementservice.md) uma instância de [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) pode ser recuperada usando essa associação.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe \_ SystemExportSettingData Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SystemExportSettingData Msvm** tem essas propriedades.

<dl> <dt>

**Iscurrent**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração referenciada está sendo usada atualmente na operação do elemento ou se essas informações são desconhecidas. Essa propriedade é herdada de [**\_ ElementSettingData do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Valor                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Current<br/>     |
| <dl> <dt>2</dt> </dl> | Não atual<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração referenciada é uma configuração padrão para o elemento ou se essas informações são desconhecidas. Essa propriedade é herdada de [**\_ ElementSettingData do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Valor                                                                        | Significado                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Padrão<br/>     |
| <dl> <dt>2</dt> </dl> | Não padrão<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a configuração referenciada é ou não a próxima configuração a ser aplicada. Por exemplo, o aplicativo pode ocorrer em uma solicitação de reinicialização, redefinição e reconfiguração. Essa pode ser uma configuração permanente ou uma configuração usada apenas uma vez, conforme indicado pelo sinalizador . Se for uma configuração permanente, a configuração será aplicada sempre que o elemento gerenciado reinicializar, até que esse sinalizador seja redefinido manualmente. No entanto, se for de uso único, o sinalizador será automaticamente limpo depois que as configurações são aplicadas. Além disso, se esse sinalizador for especificado (ou seja, definido como um valor diferente de 0 (Desconhecido), isso terá precedência sobre quaisquer dados de configuração que possam ter sido especificados como padrão. Por exemplo: se o elemento gerenciado for um sistema de computador e o valor desse sinalizador for 1 (é Próximo), a configuração estará em vigor na próxima vez que o sistema for redefinido. E, a menos que esse sinalizador seja alterado, ele persistirá para as redefinições subsequentes do sistema. No entanto, se esse sinalizador for definido como 3 (é o próximo para uso único), essa configuração será usada apenas uma vez e o sinalizador será redefinido depois disso como 2 (Não é Próximo). Portanto, no exemplo acima, se o sistema for reinicializado em uma sucessão rápida, a configuração não será usada na segunda reinicialização.

Essa propriedade é herdada de [**\_ ElementSettingData do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Valor                                                                        | Significado                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>                |
| <dl> <dt>1</dt> </dl> | É o próximo<br/>                |
| <dl> <dt>2</dt> </dl> | Não é o próximo<br/>            |
| <dl> <dt>3</dt> </dl> | É o próximo para uso único<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Cim \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData.ManagedElement")
</dt> </dl>

Referência à máquina virtual. Essa propriedade é herdada de [**\_ ElementSettingData do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)

</dd> <dt>

**Settingdata**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData.SettingData")
</dt> </dl>

Referência aos dados de configuração de exportação para a máquina virtual. Essa propriedade é herdada de [**\_ ElementSettingData do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe \_ SystemExportSettingData do Msvm** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

