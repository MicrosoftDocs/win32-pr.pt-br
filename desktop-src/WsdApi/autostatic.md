---
description: Indica se o WsdCodeGen deve ou não tentar sinalizar automaticamente determinados campos gerados como estáticos.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: Elemento autoStatic
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f6b9a447e964c90354c909fc0399276d8ed69e7d1dfb3a493d5590a6470d0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738669"
---
# <a name="autostatic-element"></a>Elemento autoStatic

Indica se o WsdCodeGen deve ou não tentar sinalizar automaticamente determinados campos gerados como estáticos. Esse comportamento é habilitado por padrão.

## <a name="usage"></a>Uso

``` syntax
<autoStatic/>
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

O **elemento autoStatic** não é necessário e pode ser omitido do arquivo de configuração XML. O elemento pode ser usado para desabilitar a sinalização de campos gerados como estáticos ou para forçar explicitamente a sinalização de determinados campos gerados como estáticos.

Os valores possíveis são 1 (habilitado, padrão) e 0 (desabilitado). A habilitação **de autoStatic** pode causar problemas de compilação, dependendo de como o gerador de código é direcionado para os dados de saída.

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




