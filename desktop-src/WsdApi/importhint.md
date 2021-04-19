---
description: 'Especifica o local de download para uma diretiva WSDL: Import que não especifica explicitamente um local.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29fcd65f9af02b8077ba828081ac9ed767d64e3
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380650"
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



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




