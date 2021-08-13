---
title: Método StopAll
description: Método StopAll
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
# <a name="stopall-method"></a>Método StopAll

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Interrompe todas as solicitações de animação ou tipos especificados de solicitações para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Tipo StopAll_ *  \[ \]



| Parte   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Tipo* | Opcional. Para usar esse parâmetro, você pode usar qualquer um dos valores a seguir. Você também pode especificar vários tipos separando-os com vírgulas. <br/> "**Get**" <br/> Para interromper todas as solicitações [**Get**](get-method.md) na fila.<br/> "**NonQueuedGet**" <br/> Para interromper todas as [](get-method.md) solicitações Get não enfiladas (**Obter** método com o parâmetro **Queue** definido como **False**).<br/> **"Mover"** <br/> Para interromper todas as solicitações [**MoveTo na fila.**](moveto-method.md)<br/> "**Reproduzir**" <br/> Para interromper todas as solicitações [**do Play na**](play-method.md) fila.<br/> "**Speak**" <br/> Para interromper todas as solicitações [**de Fala na**](speak-method.md) fila.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você não definir o parâmetro **Type,** o servidor para todas as animações do [](get-method.md) caractere, incluindo solicitações Get enfilfiladas e não enfilfiladas, e limpa sua fila de animação. Ele também para de tocar a animação Ocultando ou Mostrando de um caractere.

Esse método não gerará um [**objeto Request.**](/windows/desktop/lwef/the-request-object)

## <a name="see-also"></a>Consulte Também

[**Método Stop**](stop-method.md)


 

