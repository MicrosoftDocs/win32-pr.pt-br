---
description: Define o número da camada de código a ser gerada.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169799"
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



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




