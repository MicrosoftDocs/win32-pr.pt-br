---
description: Define os metadados de modelo e fabricante para o dispositivo a ser implementado. Este elemento é usado apenas para implementações de dispositivo (hosts).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872bcdfcf3f93bfc8fe307684c31cdebb2000b05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995333"
---
# <a name="thismodelmetadata-element"></a>elemento thisModelMetadata

Define os metadados de modelo e fabricante para o dispositivo a ser implementado. Este elemento é usado apenas para implementações de dispositivo (hosts).

## <a name="usage"></a>Uso

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                     | Descrição                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**manufacturer**](manufacturer.md)<br/>             | Nome do fabricante. Pelo menos um dos [**fabricantes**](manufacturer.md) ou [**manufacturerLS**](manufacturerls.md) deve estar presente nos metadados.<br/> <br/> |
| [**manufacturerLS**](manufacturerls.md)<br/>         | Versão localizada do nome do fabricante.<br/> <br/>                                                                                                                 |
| [**manufacturerURL**](manufacturerurl.md)<br/>       | Endereço URL do fabricante.<br/> <br/>                                                                                                                                   |
| [**modelName**](modelname.md)<br/>                   | Nome do dispositivo. Pelo menos um de [**ModelName**](modelname.md) ou [**modelNameLS**](modelnamels.md) deve estar presente nos metadados.<br/> <br/>                   |
| [**modelNameLS**](modelnamels.md)<br/>               | Versão localizada do nome do dispositivo.<br/> <br/>                                                                                                                       |
| [**modelNumber**](modelnumber.md)<br/>               | O número do modelo do dispositivo.<br/> <br/>                                                                                                                                 |
| [**modelURL**](modelurl.md)<br/>                     | Endereço de URL para o modelo de dispositivo.<br/> <br/>                                                                                                                           |
| [**PnPXDeviceCategory**](pnpxdevicecategory.md)<br/> | Categoria PnP-X à qual o dispositivo pertence. <br/> <br/>                                                                                                                |
| [**presentationURL**](presentationurl.md)<br/>       | Endereço URL dos dados de apresentação do modelo do dispositivo.<br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                                     | Descrição                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentários

Os metadados do fabricante correspondem à seção de metadados do fabricante descrita no perfil do dispositivo (consulte o perfil do dispositivo para obter detalhes). O nome do fabricante ou pelo menos uma versão localizada do nome do fabricante deve ser fornecido. O nome do modelo ou pelo menos uma versão localizada do nome do modelo deve ser fornecido.

O elemento [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) é usado subsequentemente para gerar uma constante C que contém essas informações.

Se um elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) estiver presente, pelo menos um elemento [**hospedado**](hosted.md) deverá conter ambos os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) . Da mesma forma, se os elementos **PnPXHardwareId** e **PnPXCompatibleId** estiverem presentes em um elemento **hospedado** , um elemento **PnPXDeviceCategory** deverá estar presente dentro do elemento **thisModelMetadata** .

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




