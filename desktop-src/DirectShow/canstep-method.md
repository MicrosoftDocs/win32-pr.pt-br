---
description: O método CanStep determina se o decodificador MPEG-2 no sistema local pode executar a execução de quadro em uma direção especificada.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Método CanStep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6ca29443e059cd5ebfbbb553f67cf50b1cb13e1bc8d7199ac6cfae704cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017584"
---
# <a name="canstep-method"></a>Método CanStep

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `CanStep` método determina se o decodificador MPEG-2 no sistema local pode executar a execução de quadro em uma direção especificada.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

Booliana usada como um sinalizador para especificar a direção, para frente ou para trás da capacidade de passo a passo do decodificador.



| Valor | Descrição                                          |
|-------|------------------------------------------------------|
| true  | O decodificador pode retroceder?                           |
| false | O decodificador pode avançar? Esse é o valor padrão. |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará um valor boolano de true se o decodificador puder entrar na direção especificada e false caso contrário.

## <a name="remarks"></a>Comentários

Nem todos os decodificadores mpEG-2 de hardware suportam os novos recursos de passo a passo de quadro DirectShow® 8.0. Esse método consulta o decodificador para suas funcionalidades de passo a passo de quadro. Se o decodificador puder executar a etapa do quadro, um aplicativo poderá usar o [**método Step**](step-method.md) para passar por quadros. Esse método sempre retornará **true se** um decodificador de software estiver sendo usado.

 

 



