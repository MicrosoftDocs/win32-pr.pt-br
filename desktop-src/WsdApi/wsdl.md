---
description: Especifica um arquivo WSDL para processar informações de contrato.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169639"
---
# <a name="wsdl-element"></a>elemento wsdl

Especifica um arquivo WSDL para processar informações de contrato.

## <a name="usage"></a>Uso

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                           | Descrição                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**excludeImport**](excludeimport.md)<br/> | Impede a geração de instruções de importação para destinos especificados nomeados em um elemento <WSDL: Import> em um arquivo WSDL. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Especifica o local de download para uma diretiva <WSDL: Import> que não especifica explicitamente um local.<br/> <br/>           |
| [**Multi-Path**](path.md)<br/>                   | Arquivo e caminho do arquivo de entrada WSDL.<br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                                     | Descrição                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentários

Todos os elementos [**importHint**](importhint.md) ou [**excludeImport**](excludeimport.md) que aparecem após o elemento [**Path**](path.md) em um arquivo de configuração XML serão ignorados.

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




