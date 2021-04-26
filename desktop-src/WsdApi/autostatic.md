---
description: Indica se WsdCodeGen deve tentar sinalizar automaticamente determinados campos gerados como estáticos.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: elemento autoestático
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994923"
---
# <a name="autostatic-element"></a>elemento autoestático

Indica se WsdCodeGen deve tentar sinalizar automaticamente determinados campos gerados como estáticos. Esse comportamento é habilitado por padrão.

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

O elemento **autostatic** não é obrigatório e pode ser omitido do arquivo de configuração XML. O elemento pode ser usado para desabilitar a sinalização de campos gerados como estático ou para forçar explicitamente a sinalização de determinados campos gerados como estáticos.

Os valores possíveis são 1 (habilitado, padrão) e 0 (desabilitado). Habilitar o **autostatic** pode causar problemas de compilação dependendo de como o gerador de código é direcionado para os dados de saída.

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




