---
description: Especifica um arquivo WSDL a ser processado para obter informações de contrato.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: Elemento wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158141fb8afdc216c47639f6bbb50c1d399e25f202ebbdd2f0a2c045859bffb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049514"
---
# <a name="wsdl-element"></a>Elemento wsdl

Especifica um arquivo WSDL a ser processado para obter informações de contrato.

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
| [**excludeImport**](excludeimport.md)<br/> | Impede a geração de instruções de importação para destinos especificados nomeados \<wsdl:import> em um elemento em um arquivo WSDL. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Especifica o local de download de uma \<wsdl:import> diretiva que não especifica explicitamente um local.<br/> <br/>           |
| [**Caminho**](path.md)<br/>                   | Arquivo e caminho do arquivo de entrada WSDL.<br/> <br/>                                                                                      |



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

Todos [**os elementos importHint**](importhint.md) ou [**excludeImport**](excludeimport.md) exibidos após o elemento [**path**](path.md) em um arquivo de configuração XML serão ignorados.

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




