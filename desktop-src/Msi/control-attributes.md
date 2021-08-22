---
description: Para obter informações sobre atributos de controle, consulte o link para o controle específico que você precisa criar em controles, bem como os links para determinados atributos de controle nas listas a seguir.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Atributos de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9d7412ce3893b785dccf067287c191f033bdf5a100628577260ff10f74ce1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500716"
---
# <a name="control-attributes"></a>Atributos de controle

Para obter informações sobre atributos de controle, consulte o link para o controle específico que você precisa criar em [controles](controls.md) , bem como os links para determinados atributos de controle nas listas a seguir.

Os métodos a seguir são usados para especificar os atributos de um controle:

-   Use a [tabela ControlCondition](controlcondition-table.md) para desabilitar, habilitar, ocultar ou mostrar um controle de acordo com o valor de uma propriedade ou instrução condicional. Você também pode usar essa tabela para substituir o controle padrão especificado na [tabela de diálogo](dialog-table.md).
-   Assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md). Insira o identificador do atributo na coluna de atributo e o identificador do ControlEvent, na coluna evento desta tabela.
-   Defina os sinalizadores de bit de atributo de controle para o controle na coluna atributo da [tabela de controle](control-table.md). Isso define os atributos na criação do controle.

Alguns atributos não podem ser definidos para cada controle ou ser especificados por todos os métodos acima. Consulte os tópicos de controle e atributo específicos para obter detalhes.

Os valores iniciais de alguns atributos de controle podem ser definidos com bits na [tabela de controle](control-table.md).



| Atributo                                          | Decimal | Hexadecimal | Constante                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [BiDi](bidi-control-attribute.md)                 | 224     | 0x000000E0  | **msidbControlAttributesBiDi**         |
| [Habilitada](enabled-control-attribute.md)           | 2       | 0x00000002  | **msidbControlAttributesEnabled**      |
| [Indireto.](indirect-control-attribute.md)         | 8       | 0x00000008  | **msidbControlAttributesIndirect**     |
| [Controle de inteiro](integer-control-attribute.md)   | 16      | 0x00000010  | **msidbControlAttributesInteger**      |
| [LeftScroll](leftscroll-control-attribute.md)     | 128     | 0x00000080  | **msidbControlAttributesLeftScroll**   |
| [RightAligned](rightaligned-control-attribute.md) | 64      | 0x00000040  | **msidbControlAttributesRightAligned** |
| [RTLRO](rtlro-control-attribute.md)               | 32      | 0x00000020  | **msidbControlAttributesRTLRO**        |
| [Submersa](sunken-control-attribute.md)             | 4       | 0x00000004  | **msidbControlAttributesSunken**       |
| [Visível](visible-control-attribute.md)           | 1       | 0x00000001  | **msidbControlAttributesVisible**      |



 

Esses atributos de controles de texto são definidos com bits.



| Atributo                                            | Decimal | Hexadecimal | Constante                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [Formatar](formatsize-control-attribute.md)       | 524288  | 0x00080000  | **msidbControlAttributesFormatSize**    |
| [NoPrefix](noprefix-control-attribute.md)           | 131072  | 0x00020000  | **msidbControlAttributesNoPrefix**      |
| [Desencapsular](nowrap-control-attribute.md)               | 262144  | 0x00040000  | **msidbControlAttributesNoWrap**        |
| [Senha](password-control-attribute.md)           | 2097152 | 0x00200000  | **msidbControlAttributesPasswordInput** |
| [Transparente](transparent-control-attribute.md)     | 65536   | 0x00010000  | **msidbControlAttributesTransparent**   |
| [UsersLanguage](userslanguage-control-attribute.md) | 1048576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

Esse atributo do controle ProgressBar é definido com um bit.



| Atributo                                      | Decimal | Hexadecimal | Constante                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [Progress95](progress95-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

Esses atributos dos controles SelectCombo de volume e de diretório são definidos com bits.



| Atributo                                                | Decimal | Hexadecimal | Constante                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [CDROMVolume](cdromvolume-control-attribute.md)         | 524288  | 0x00080000  | **msidbControlAttributesCDROMVolume**     |
| [FixedVolume](fixedvolume-control-attribute.md)         | 131072  | 0x00020000  | **msidbControlAttributesFixedVolume**     |
| [FloppyVolume](floppyvolume-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume**    |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)     | 1048576 | 0x00100000  | **msidbControlAttributesRAMDiskVolume**   |
| [RemoteVolume](remotevolume-control-attribute.md)       | 262144  | 0x00040000  | **msidbControlAttributesRemoteVolume**    |
| [RemovableVolume](removablevolume-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

Esses atributos dos controles ListBox e ComboBox são definidos com bits.



| Atributo                                            | Decimal | Hexadecimal | Constante                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [Controle de combinação de combinações](combolist-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesComboList** |
| [Controle classificado](sorted-control-attribute.md)       | 65536   | 0x00010000  | **msidbControlAttributesSorted**    |



 

Esse atributo do controle de edição é definido com um bit.



| Atributo                                    | Decimal | Hexadecimal | Constante                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [Tiverem](multiline-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

Esses atributos de controles PictureButton são definidos com bits.



| Atributo                                          | Decimal | Hexadecimal | Constante                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [Bitmap](bitmap-control-attribute.md)             | 262144  | 0x00040000  | **msidbControlAttributesBitmap**     |
| [FixedSize](fixedsize-control-attribute.md)       | 1048576 | 0x00100000  | **msidbControlAttributesFixedSize**  |
| [Ícone](icon-control-attribute.md)                 | 524288  | 0x00080000  | **msidbControlAttributesIcon**       |
| [IconSize16](iconsize-control-attribute.md)       | 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| [IconSize32](iconsize-control-attribute.md)       | 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| [IconSize48](iconsize-control-attribute.md)       | 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |
| [Controle PushLike](pushlike-control-attribute.md) | 131072  | 0x00020000  | **msidbControlAttributesPushLike**   |



 

Esse atributo do controle RadioButton é definido com um bit.



| Atributo                                    | Decimal  | Hexadecimal | Constante                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [HasBorder](hasborder-control-attribute.md) | 16777216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

Esse atributo de controle de supressão é definido com um bit.



| Atributo                                        | Decimal | Hexadecimal | Constante                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [ElevationShield](elevationshield-attribute.md) | 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

Esse atributo do controle VolumeCostList é definido com um bit.



| Atributo                                                                | Decimal | Hexadecimal | Constante                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [ControlShowRollbackCost](controlshowrollbackcost-control-attribute.md) | 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

Os atributos de controle a seguir não são definidos com bits. Esses atributos são criado nas tabelas de interface do usuário ou são definidos usando [Eventos de Controle](control-events.md).

[NomedoMál](billboardname-control-attribute.md)

 

[IndirectPropertyName](indirectpropertyname-control-attribute.md)

 

[Posição](position-control-attribute.md)

 

[Controle de progresso](progress-control-attribute.md)

 

[PropertyName](propertyname-control-attribute.md)

 

[PropertyValue](propertyvalue-control-attribute.md)

 

[Text Control](text-control-attribute.md)

 

[TimeRemaining](timeremaining-control-attribute.md)

Consulte [Adicionando controles e texto.](adding-controls-and-text.md)

 

 



