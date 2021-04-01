---
description: O método canstep determina se o decodificador MPEG-2 no sistema local pode executar a revisão do quadro em uma direção especificada.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Método canstep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009917"
---
# <a name="canstep-method"></a>Método canstep

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `CanStep` método determina se o decodificador MPEG-2 no sistema local pode executar a revisão do quadro em uma direção especificada.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

Booliano usado como um sinalizador para especificar a direção, encaminhamento ou retrocesso da capacidade de depuração de quadro do decodificador.



| Valor | Descrição                                          |
|-------|------------------------------------------------------|
| true  | A etapa do decodificador pode voltar?                           |
| false | O decodificador pode avançar? Esse é o valor padrão. |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano de true se o decodificador puder entrar na direção especificada e false caso contrário.

## <a name="remarks"></a>Comentários

Nem todos os decodificadores de hardware MPEG-2 dão suporte aos novos recursos de revisão de quadros no DirectShow® 8,0. Esse método consulta o decodificador para seus recursos de revisão de quadros. Se o decodificador puder executar a revisão do quadro, um aplicativo poderá usar o método [**Step**](step-method.md) para percorrer os quadros. Esse método sempre retornará **true** se um decodificador de software estiver sendo usado.

 

 



