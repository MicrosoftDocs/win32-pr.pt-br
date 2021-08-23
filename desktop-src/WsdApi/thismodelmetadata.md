---
description: Define o fabricante e os metadados do modelo para o dispositivo a ser implementado. Esse elemento é usado somente para implementações de dispositivo (hosts).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: Elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01d074e7e9c8d43e078ebc477366d88608e7c4f3fade6c0be3dbc6fda23f006b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991546"
---
# <a name="thismodelmetadata-element"></a>Elemento thisModelMetadata

Define o fabricante e os metadados do modelo para o dispositivo a ser implementado. Esse elemento é usado somente para implementações de dispositivo (hosts).

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
| [**fabricante**](manufacturer.md)<br/>             | Nome do fabricante. Pelo menos um fabricante [**ou**](manufacturer.md) [**fabricanteLS**](manufacturerls.md) deve estar presente nos metadados.<br/> <br/> |
| [**manufacturerLS**](manufacturerls.md)<br/>         | Versão localizada do nome do fabricante.<br/> <br/>                                                                                                                 |
| [**Manufacturerurl**](manufacturerurl.md)<br/>       | Endereço da URL do fabricante.<br/> <br/>                                                                                                                                   |
| [**Modelname**](modelname.md)<br/>                   | Nome do dispositivo. Pelo menos um de [**modelName**](modelname.md) ou [**modelNameLS**](modelnamels.md) deve estar presente nos metadados.<br/> <br/>                   |
| [**modelNameLS**](modelnamels.md)<br/>               | Versão localizada do nome do dispositivo.<br/> <br/>                                                                                                                       |
| [**modelNumber**](modelnumber.md)<br/>               | Número do modelo do dispositivo.<br/> <br/>                                                                                                                                 |
| [**modelURL**](modelurl.md)<br/>                     | Endereço de URL para o modelo de dispositivo.<br/> <br/>                                                                                                                           |
| [**PnPXDeviceCategory**](pnpxdevicecategory.md)<br/> | Categoria PnP-X à qual o dispositivo pertence. <br/> <br/>                                                                                                                |
| [**presentationURL**](presentationurl.md)<br/>       | Endereço de URL dos dados de apresentação do modelo de dispositivo.<br/> <br/>                                                                                                        |



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

Os metadados do fabricante corresponde à seção de metadados do fabricante descrita no perfil do dispositivo (consulte o perfil do dispositivo para obter detalhes). O nome do fabricante ou pelo menos uma versão localizada do nome do fabricante deve ser fornecida. O nome do modelo ou pelo menos uma versão localizada do nome do modelo deve ser fornecida.

O [**elemento thisModelMetadataDefinition**](thismodelmetadatadefinition.md) é usado posteriormente para gerar uma constante C que contém essas informações.

Se um [**elemento PnPXDeviceCategory**](pnpxdevicecategory.md) estiver presente, pelo menos um elemento hospedado deverá conter elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId.**](pnpxcompatibleid.md) [](hosted.md) Da mesma forma, se os elementos **PnPXHardwareId** e  **PnPXCompatibleId** estão presentes em um elemento hospedado, um elemento **PnPXDeviceCategory** deve estar presente dentro do elemento **thisModelMetadata.**

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




