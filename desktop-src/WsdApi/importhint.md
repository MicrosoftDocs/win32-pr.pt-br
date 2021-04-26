---
description: 'Especifica o local de download para uma diretiva WSDL: Import que não especifica explicitamente um local.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c874879ee0a608c100f32a0520a85efe76080cc2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998753"
---
# <a name="importhint-element"></a>elemento importHint

Especifica o local de download para uma \<wsdl:import> diretiva que não especifica explicitamente um local.

## <a name="usage"></a>Uso

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**local**](location.md)<br/>   | O local do arquivo a ser importado. O local pode ser um caminho relativo, um caminho absoluto ou uma URL HTTP.<br/> <br/> |
| [**nameSpace**](namespace.md)<br/> | O namespace a ser importado. Isso deve corresponder ao namespace especificado no \<wsdl:import> elemento.<br/> <br/>     |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**WSDL**](wsdl.md)<br/> | Especifica um arquivo WSDL para processar informações de contrato.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




