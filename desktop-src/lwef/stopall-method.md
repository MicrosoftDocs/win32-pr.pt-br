---
title: Método do opAll
description: Método do opAll
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b138be6ea75135d5ddefdea9e1e5cc120d875ae092478ad3147332720e5a0907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745938"
---
# <a name="stopall-method"></a>Método do opAll

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Interrompe todas as solicitações de animação ou tipos especificados de solicitações para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_"). Tipo de interopall_ *  \[ \]



| Parte   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Tipo* | Opcional. Para usar esse parâmetro, você pode usar qualquer um dos valores a seguir. Você também pode especificar vários tipos separando-os com vírgulas. <br/> "**Obter**" <br/> Para interromper todas as solicitações [**Get**](get-method.md) em fila.<br/> "**NonQueuedGet**" <br/> Para interromper todas as solicitações [**Get**](get-method.md) não enfileiradas (método **Get** com o parâmetro **Queue** definido como **false**).<br/> "**Mover**" <br/> Para interromper todas as solicitações [**MoveTo**](moveto-method.md) enfileiradas.<br/> "**Reproduzir**" <br/> Para interromper todas as solicitações de [**reprodução**](play-method.md) em fila.<br/> "**Fale**" <br/> Para interromper todas as solicitações de [**fala**](speak-method.md) enfileiradas.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você não definir o parâmetro de **tipo** , o servidor interromperá todas as animações para o caractere, incluindo solicitações [**Get**](get-method.md) enfileiradas e não enfileiradas, e limpará sua fila de animação. Ele também interrompe a reprodução de uma animação de ocultar ou mostrar um caractere.

Esse método não gerará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>Consulte Também

[**Método Stop**](stop-method.md)


 

