---
description: O objeto ConfigurableItem representa uma única linha da Tabela ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Objeto ConfigurableItem (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752049"
---
# <a name="configurableitem-object"></a>Objeto ConfigurableItem

O **objeto ConfigurableItem** representa uma única linha da [Tabela ModuleConfiguration](moduleconfiguration-table.md). Esse é um "atributo" único configurável do módulo. A interface consiste em propriedades somente leitura, uma para cada coluna na Tabela ModuleConfiguration. A definição da interface é a seguinte:

## <a name="members"></a>Membros

O objeto **ConfigurableItem** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **ConfigurableItem** tem essas propriedades.



| Propriedade                                                         | Descrição                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atributos**](configurableitem-attributes.md)<br/>     | Retorna o valor no campo atributos do registro desse objeto na Tabela ModuleConfiguration.<br/>                            |
| [**Contexto**](configurableitem-context.md)<br/>           | Retorna o valor no campo de contexto do registro desse objeto na Tabela ModuleConfiguration.<br/>                               |
| [**DefaultValue**](configurableitem-defaultvalue.md)<br/> | Retorna o valor no campo DefaultValue do registro desse objeto na Tabela ModuleConfiguration.<br/>                          |
| [**Descrição**](configurableitem-description.md)<br/>   | Retorna o valor no campo Descrição do registro desse objeto na Tabela ModuleConfiguration.<br/>                           |
| [**DisplayName**](configurableitem-displayname.md)<br/>   | Retorna o valor no campo DisplayName do registro desse objeto na Tabela ModuleConfiguration.<br/>                           |
| [**Formatar**](configurableitem-format.md)<br/>             | Retorna o valor no campo formato do registro desse objeto na Tabela ModuleConfiguration.<br/>                                |
| [**HelpKeyword**](configurableitem-helpkeyword.md)<br/>   | Retorna o valor no campo HelpKeyword do registro desse objeto na Tabela ModuleConfiguration.<br/>                           |
| [**HelpLocation**](configurableitem-helplocation.md)<br/> | Retorna o valor no campo HelpLocation do registro desse objeto na Tabela ModuleConfiguration.<br/>                          |
| [**Nome**](configurableitem-name.md)<br/>                 | Retorna o valor no campo nome do registro desse objeto na [Tabela ModuleConfiguration](moduleconfiguration-table.md).<br/> |
| [**Tipo**](configurableitem-type.md)<br/>                 | Retorna o valor no campo tipo do registro desse objeto na Tabela ModuleConfiguration.<br/>                                  |



 

## <a name="c"></a>C++

IMsmConfigurableItem de interface **: IDispatch**

## <a name="interface-id"></a>ID da interface



| Constante                      | Valor                                  |
|-------------------------------|----------------------------------------|
| **IMsmConfigurableItem de IID \_** | {4D6E6284-D21D-401E-84F6-909E00B50F71} |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




