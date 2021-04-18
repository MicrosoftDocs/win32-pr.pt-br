---
description: O método step avança o DVD-Video fluxo pelo número especificado de quadros.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Método Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789678"
---
# <a name="step-method"></a>Método Step

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `Step` método avança o DVD-Video fluxo pelo número especificado de quadros.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Especifica o número de quadros para a etapa como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, chame [**canstep**](canstep-method.md) para determinar se o decodificador dá suporte à revisão de quadros.

Se o DVD-Video estiver sendo executado no modo reverso quando esse método for chamado e o decodificador der suporte à revisão de quadro reverso, a etapa do quadro será feita em ordem inversa.

 

 



