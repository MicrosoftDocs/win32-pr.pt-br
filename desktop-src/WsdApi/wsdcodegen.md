---
description: É o elemento raiz de um arquivo de script XML do gerador de código WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: elemento wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812327"
---
# <a name="wsdcodegen-element"></a>elemento wsdCodeGen

É o elemento raiz de um arquivo de script XML do gerador de código WSDAPI.

## <a name="usage"></a>Uso

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a>Atributos



| Atributo                        | Type                             | Obrigatório       | Descrição                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| **ConfigFileVersion**<br/> | Qualquer cadeia de caracteres.<br/> | Yes<br/> | A versão do arquivo de configuração. O único valor válido é "1,0".<br/> <br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                         | Descrição                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**autoestático**](autostatic.md)<br/>                     | Indica se WsdCodeGen deve tentar sinalizar automaticamente determinados campos gerados como estáticos. Isso é habilitado por padrão.<br/> <br/>                                                                 |
| [**Grupo**](file.md)<br/>                                 | Direciona o gerador de código para gerar um arquivo.<br/> <br/>                                                                                                                                                       |
| [**hostMetadata**](hostmetadata.md)<br/>                 | Os metadados de hospedagem para o dispositivo a ser implementado. Este elemento é usado apenas para implementações de dispositivo (hosts).<br/> <br/>                                                                                 |
| [**layerNumber**](layernumber.md)<br/>                   | O número da camada de código a ser gerada. Os números de camada são usados em tabelas de tempo de execução para distinguir uma camada de código para outra. O WSDAPI usa o código gerado que tem um número de camada de 0.<br/> <br/> |
| [**layerPrefix**](layerprefix.md)<br/>                   | O prefixo a ser usado no código gerado para garantir a exclusividade dos símbolos gerados. O WSDAPI usa o prefixo "WSD".<br/> <br/>                                                                                     |
| [**Ela**](macro.md)<br/>                               | Define o texto ou CDATA a ser reutilizado pelo elemento [**include**](include.md) .<br/> <br/>                                                                                                                        |
| [**nameSpace**](namespace.md)<br/>                       | Descreve um namespace a ser usado para geração de código.<br/> <br/>                                                                                                                                                |
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Descreve o host e os metadados hospedados para o dispositivo.<br/> <br/>                                                                                                                                               |
| [**thisModelMetadata**](thismodelmetadata.md)<br/>       | Os metadados de modelo e fabricante para o dispositivo a ser implementado. Este elemento é usado apenas para implementações de dispositivo (hosts).<br/> <br/>                                                                  |
| [**WSDL**](wsdl.md)<br/>                                 | Especifica um arquivo WSDL para processar informações de contrato.<br/> <br/>                                                                                                                                           |
| [**XSD**](xsd.md)<br/>                                   | Especifica um arquivo XSD para processar informações de contrato.<br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a>Elementos pai

Não há elementos pai.

## <a name="remarks"></a>Comentários

Em geral, os elementos de [**arquivo**](file.md) devem ocorrer por último porque geram código que usa os dados especificados pelos outros elementos.

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




