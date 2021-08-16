---
description: Define o número da camada de código a ser gerada.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603815fc178cb02df0eeb33e6ad856076b99b8ea582574703078323b36ba1cbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130768"
---
# <a name="layernumber-element"></a>elemento layerNumber

Define o número da camada de código a ser gerada.

## <a name="usage"></a>Uso

``` syntax
<layerNumber/>
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

Os números de camada são usados em tabelas de tempo de execução para distinguir uma camada de código para outra. O WSDAPI usa o código gerado que tem um número de camada de 0.

Normalmente, esse valor será 1, indicando que o código gerado está em camadas na parte superior do WSDAPI e nenhuma outra camada. Em alguns casos, números mais altos podem ser usados. Por exemplo, se uma empresa produz código para uma classe de dispositivo (camada numerada 1), um fornecedor de hardware específico pode desejar adicionar uma camada 2 de número de camada adicional.

Os valores válidos, exceto no caso do WSDAPI em si, são maiores que 0 e menores que 16.

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




