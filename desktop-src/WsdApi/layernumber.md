---
description: Define o número da camada de código a ser gerada.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995483"
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



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




