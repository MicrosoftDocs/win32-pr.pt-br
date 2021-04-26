---
description: Define os metadados de hospedagem para o dispositivo a ser implementado. Este elemento é usado apenas para implementações de dispositivo (hosts).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994793"
---
# <a name="hostmetadata-element"></a>elemento hostMetadata

Define os metadados de hospedagem para o dispositivo a ser implementado. Este elemento é usado apenas para implementações de dispositivo (hosts).

## <a name="usage"></a>Uso

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                             | Descrição                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**hospedeira**](host.md)<br/>     | Define os elementos ServiceId e [**Types**](types.md) para o host de serviço. Se não for fornecido explicitamente, o WSDAPI não fornecerá nenhum dado padrão em resposta a solicitações de metadados.<br/> <br/>                                                                                                                                          |
| [**hospedado**](hosted.md)<br/> | Define os elementos [**ServiceId**](serviceid.md) e [**Types**](types.md) para os serviços fornecidos por esse host de serviço. Cada serviço fornecido por esse host de serviço deve ter suas próprias informações de elemento [**hospedado**](hosted.md) para garantir que o serviço seja publicado corretamente em respostas a solicitações de metadados.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                         | Descrição                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Descreve o host e os metadados hospedados para o dispositivo.<br/> <br/> |



## <a name="remarks"></a>Comentários

Os metadados de hospedagem aparecem nesse elemento em um formato semelhante ao especificado no perfil do dispositivo. **hostMetadata** é um pouco diferente do formato descrito no perfil do dispositivo no qual a única propriedade de referência à qual ele dá suporte é a ID do serviço.

O elemento [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) é usado subsequentemente para gerar uma constante C que contém essas informações.

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




