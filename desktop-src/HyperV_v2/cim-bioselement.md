---
description: Representa o software de nível baixo que é carregado no armazenamento não volátil e usado para iniciar e configurar um sistema de computador (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: Classe CIM_BIOSElement (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 78f2433d2b75e2c348fdf6e7a8ff35db56c9a0c8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879876"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>Classe CIM_BIOSElement (gerenciamento do Hyper-V)

Representa o software de nível baixo que é carregado no armazenamento não volátil e usado para iniciar e configurar um sistema de computador ([**CIM \_ ComputerSystem**](cim-computersystem.md)).

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a>Membros

A classe **CIM \_ bioselement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ bioselement** tem essas propriedades.

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ bioselement**.**ListOfLanguages**")
</dt> </dl>

O idioma selecionado no momento para o BIOS. Essas informações podem ser obtidas no BIOS de gerenciamento do sistema (SMBIOS) usando o atributo de idioma atual da estrutura do tipo 13 para indexar na lista de cadeias de caracteres que segue a estrutura. Essa propriedade é formatada usando o nome da linguagem ISO 639 e pode ser seguida pelo nome da região ISO 3166 e pelo método de codificação.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma lista de idiomas instaláveis para o BIOS. Essas informações podem ser obtidas no SMBIOS, na lista de cadeias de caracteres que segue a estrutura do tipo 13. Um nome de idioma ISO 639 deve ser usado para especificar os idiomas instaláveis do BIOS. O nome da região ISO 3166 e o método de codificação também podem ser especificados, seguindo o nome do idioma.

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,6 ")
</dt> </dl>

O endereço final da memória ocupada pelo BIOS.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,5 ")
</dt> </dl>

O endereço inicial da memória ocupada pelo BIOS.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,7 ")
</dt> </dl>

Uma cadeia de caracteres de forma livre que descreve o Utilitário Flash/carregamento do BIOS necessário para atualizar o objeto **CIM \_ bioselement** . A versão e outras informações podem ser indicadas nesta propriedade.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("fabricante"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,2 ")
</dt> </dl>

O fabricante do elemento de software.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,9 ")
</dt> </dl>

True se este for o principal BIOS do sistema de computador; caso contrário, false.

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O local de publicação dos registros de atributo do BIOS para os quais a implementação do BIOS está em conformidade.

</dd> <dt>

**Liberado**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,8 ")
</dt> </dl>

A data em que este BIOS foi lançado.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,3 ")
</dt> </dl>

A versão da operação. A versão da operação deve estar em um dos seguintes formatos:

-   *&lt; principal &gt;**. &lt; secundária &gt;*. *&lt; revisão &gt;*
-   *&lt; principal &gt;**. &lt; &gt; &lt; &gt; &lt; revisão &gt; de letra secundária*

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

[**\_Software CIM**](cim-softwareelement.md)
</dt> </dl>

 

