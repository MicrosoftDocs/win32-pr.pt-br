---
title: Ocultar método
description: Ocultar método
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084506"
---
# <a name="hide-method"></a>Ocultar método

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Oculta o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). Ocultar* *  \[ *rápido*\]



| Parte   | Descrição                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rápido* | Opcional. Um valor booliano que indica se a animação associada **ao estado oculto** do caractere deve ser ignorada não reproduz a animação **oculta** . <br/> **False** (padrão) reproduz a animação de **ocultação** . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O servidor enfileira as ações do método **Hide** na fila do caractere, para que você possa usá-lo para ocultar o caractere após uma sequência de outras animações. Você pode executar a ação imediatamente usando o método [**Stop**](stop-method.md) antes de chamar esse método.

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Além disso, se a animação **oculto** associada não tiver sido carregada e você não tiver especificado o parâmetro **Fast** como **true**, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado. Portanto, se você estiver usando o protocolo HTTP para acessar dados de caractere ou de animação, use o método [**Get**](get-method.md) e especifique o estado **oculto** para carregar a animação antes de chamar o método **Hide** .

Ocultar um caractere também pode resultar no disparo do evento [**ActivateInput**](activateinput-event.md) de outro cliente.

> [!Note]  
> Os caracteres ocultos não podem acessar o canal de áudio. O servidor passará um status de falha no evento [**RequestComplete**](requestcomplete-event.md) se você gerar uma solicitação de animação e o caractere estiver oculto.

 

## <a name="see-also"></a>Consulte Também

[**Método Show**](show-method.md)


 

