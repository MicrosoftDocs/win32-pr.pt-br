---
description: Gera uma declaração para uma função que cria um host digitado.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: elemento hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf3ddd474b4000b053b49157f1fc4b2eb399d34
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994903"
---
# <a name="hostbuilderdeclaration-element"></a>elemento hostBuilderDeclaration

Gera uma declaração para uma função que cria um host digitado.

## <a name="usage"></a>Uso

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**interface**](interface.md)<br/> | O nome da interface de serviço a ser incluída para o host. O valor desse elemento deve corresponder ao valor do elemento filho da [**interface**](interface.md) do [**hostedService**](hostedservice.md). <br/> <br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
interface+
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




