---
description: O método setatrasartime define o tempo de atraso para a dica de ferramenta associada ao objeto MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ebd119f20977c98aa2664518dc2125b7b5c157b44ff53c3a37740bf40a1677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683736"
---
# <a name="setdelaytime"></a>SetDelayTime

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SetDelayTime` método define o tempo de atraso para a dica de ferramenta associada ao objeto **MSWebDVD** .

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*
</dt> <dd>

Especifica o tipo de atraso como um inteiro.



| Valor | Descrição                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | Para redefinir o tempo de atraso Autopop para o valor padrão, defina *iNewVal* como-1.                                                                                                                                                                       |
| 0     | Defina o período de tempo que uma janela de dica de ferramenta permanecerá visível se o ponteiro for estático dentro do retângulo delimitador de uma ferramenta.                                                                                                                         |
| 1     | Defina o período de tempo que um ponteiro deve permanecer fixo dentro do retângulo delimitador de uma ferramenta antes que a janela de dica de ferramentas seja exibida.                                                                                                                    |
| 2     | Defina o período de tempo que leva para que janelas de dica de ferramenta subsequentes apareçam quando o ponteiro se mover de uma das ferramentas para outra.                                                                                                                          |
| 3     | Defina todos os tempos de atraso para as proporções padrão. A hora de Autopop é dez vezes a hora inicial e o tempo de reapresentação é um quinto da hora inicial. Se esse sinalizador estiver definido, use um valor positivo de iNewVal para especificar a hora inicial, em milissegundos. |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*
</dt> <dd>

Especifica o atraso, em milissegundos, como um inteiro.



| Valor                    | Descrição                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | Define o atraso especificado em *iDelayType* para seu valor padrão |
| qualquer outro valor negativo | Define todos os tipos de atraso para o valor padrão.                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

 

 



