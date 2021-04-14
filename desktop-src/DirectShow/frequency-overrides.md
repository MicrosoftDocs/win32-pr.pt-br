---
description: Substituições de frequência
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Substituições de frequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500202"
---
# <a name="frequency-overrides"></a>Substituições de frequência

Uma quantidade significativa de esforço foi gasta para garantir que as frequências de difusão e as atribuições padrão de cor estejam corretas para cada país/região. Mesmo assim, haverá situações em que as tabelas de frequência não são suficientes, contêm erros ou se tornam obsoletas. Para resolver esse problema, as frequências listadas nas tabelas de frequência do filtro de sintonizador de TV podem ser substituídas seletivamente, usando a seguinte chave do registro:

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

> [!Note]  
> A partir do Windows 7, a seguinte chave de registro redirecionada é usada para aplicativos x86 em execução em versões x64 do Windows:

 

**HKEY \_ \_Computador local** \\ **software** \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

As substituições de frequência são agrupadas em "espaços de ajuste" definidos pelo aplicativo, que são identificadas pelo número. O exemplo a seguir mostra uma substituição de exemplo:

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

Nesse caso, "TS0-1" indica o espaço de ajuste 0 para frequências de cabo. O primeiro número identifica o espaço de ajuste. O segundo número é 0 para frequências de difusão ou 1 para frequências de cabo.

A subchave chamada "12" substitui o valor de frequência da frequência no índice 12 da tabela de frequência atual. O valor da subchave é um **DWORD** que especifica a frequência em Hertz (Hz). Neste exemplo, a frequência é definida como 67,25 MHz. As substituições podem ser definidas para qualquer número de canal no intervalo de 1 a 999, inclusive. Se o hardware de ajuste não oferecer suporte a uma determinada frequência, a solicitação de ajuste falhará.

Esse mecanismo também pode ser usado para criar novos números de canal fora do intervalo existente na tabela de frequência. O método [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) retornará o intervalo de canais estendido. Por exemplo, se o intervalo de canal original era de 1 a 158 e uma substituição de canal de "200" for adicionada ao registro, o método **ChannelMinMax** retornará 200 como o canal máximo. Nesse caso, os números de canal no intervalo de 159 a 199 não terão frequências atribuídas a eles, portanto, quaisquer solicitações de ajuste nesse intervalo falharão automaticamente.

O método [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) permite que o aplicativo escolha qual conjunto de substituições e informações de ajuste fino a serem usadas. Os números de espaço de ajuste são arbitrários. É responsabilidade do aplicativo manter a relação entre o espaço de ajuste e a tabela de frequência. A abordagem mais simples é usar o código de país/região como o número de espaço de ajuste. Em seguida, sempre que o aplicativo alternar para um novo código de país/região, ele também alternará para o mesmo espaço de ajuste (nessa ordem).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ajuste de TV analógica internacional](international-analog-tv-tuning.md)
</dt> </dl>

 

 



