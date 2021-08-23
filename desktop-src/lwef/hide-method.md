---
title: Método Hide
description: Método Hide
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67057464c8e505e56123f712d3a1e6d668c7d75b00bc4732e7b18195b3be9723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725446"
---
# <a name="hide-method"></a>Método Hide

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Oculta o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Ocultar_ *  \[ *Rápido*\]



| Parte   | Descrição                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rápido* | Opcional. Um valor booliana que indica se a animação associada  ao estado Ocultando True do caractere Não reproduz a **animação Ocultando.** <br/> **False** (Padrão) Reproduz a **animação Ocultando.** <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O servidor enfilfilia as ações do método **Hide** na fila do caractere, para que você possa usá-lo para ocultar o caractere após uma sequência de outras animações. Você pode reproduzir a ação imediatamente usando o [**método Stop**](stop-method.md) antes de chamar esse método.

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um [**objeto Request.**](/windows/desktop/lwef/the-request-object) Além disso, se  a animação Ocultação associada não tiver sido carregada e você  não tiver especificado o parâmetro **Fast** como **True**, o servidor define a propriedade [**Status**](status-property.md) do objeto Request como "failed" com um número de erro apropriado. Portanto, se você estiver usando o protocolo HTTP para acessar caracteres  ou dados de animação, use o método [**Get**](get-method.md) e especifique o estado Ocultando para carregar a animação antes de chamar o **método Hide.**

Ocultar um caractere também pode resultar no gatilho do [**evento ActivateInput**](activateinput-event.md) de outro cliente.

> [!Note]  
> Caracteres ocultos não podem acessar o canal de áudio. O servidor passará um status de falha no evento [**RequestComplete**](requestcomplete-event.md) se você gerar uma solicitação de animação e o caractere estiver oculto.

 

## <a name="see-also"></a>Consulte Também

[**Método Show**](show-method.md)


 

