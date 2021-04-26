---
description: Define o prefixo a ser usado no código gerado para garantir a exclusividade dos símbolos gerados.
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: elemento layerPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98970013c72600affd7d4d9e7a71781f477cd87d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994692"
---
# <a name="layerprefix-element"></a>elemento layerPrefix

Define o prefixo a ser usado no código gerado para garantir a exclusividade dos símbolos gerados.

## <a name="usage"></a>Uso

``` syntax
<layerPrefix/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                     | Descrição                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentários

Cada script do gerador de código deve definir uma cadeia de caracteres de prefixo exclusiva para os módulos criados. Por exemplo, os scripts de quadro de imagem usam um prefixo de "PFDEMO".

O WSDAPI usa o prefixo "WSD".

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




