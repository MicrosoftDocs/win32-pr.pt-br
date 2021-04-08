---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822954"
---
# <a name="listenstart-event"></a>Evento ListenStart

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o modo de escuta (reconhecimento de fala) é iniciado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent. * * * ListenStart (ByVal* *  *characterid * * *)**



| Parte          | Descrição                                            |
|---------------|--------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere de escuta como uma cadeia de caracteres. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento é enviado a todos os clientes quando o modo de escuta começa porque o usuário pressionou a chave de escuta ou o cliente de entrada-ativo chamou o método [**Listen**](listen-method.md) com **true**. Você pode usar esse evento para evitar que seu caractere fale enquanto o modo de escuta está ativado.

Se você ativar o modo de escuta com o método [**Listen**](listen-method.md) e, em seguida, o usuário pressionar a tecla de escuta, o modo de escuta redefinirá e continuará até que o tempo limite da chave de escuta seja concluído, a chave de escuta será liberada ou o usuário terminará de falar, o que for mais tarde. Nessa situação, quando o modo de escuta já estiver ativado, você não receberá um evento **ListenStart** adicional quando o usuário pressionar a tecla de escuta.

O evento retorna o caractere para os clientes que atualmente têm esse caractere carregado. Todos os outros clientes recebem um caractere nulo (cadeia de caracteres vazia).

### <a name="see-also"></a>Consulte Também

[**Evento ListenComplete**](listencomplete-event.md), [ **método Listen**](listen-method.md)


 

 




