---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0017b628af3ca266058de74508d379bd665c94f94c64207f4d7bef5487a0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976106"
---
# <a name="listenstart-event"></a>Evento ListenStart

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando o modo de escuta (reconhecimento de fala) começa.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *agent.***ListenStart (ByVal* *  *CharacterID***)**



| Parte          | Descrição                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | Retorna a ID do caractere de escuta como uma cadeia de caracteres. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento é enviado a todos os clientes quando o modo de Escuta começa porque o usuário pressionou a tecla Listening ou o cliente de entrada ativo chamado método [**Listen**](listen-method.md) com **True**. Você pode usar esse evento para evitar que seu caractere fale enquanto o modo de escuta está.

Se você ativar o [](listen-method.md) modo de Escuta com o método Listen e, em seguida, o usuário pressionar a tecla Listening, o modo de Escuta será redefinido e continuará até que o tempo-tempo de escuta da chave seja concluído, a tecla Listening será liberada ou o usuário terminará de falar, o que for posterior. Nessa situação, quando o modo de escuta já estiver ativa, você não obterá um evento **ListenStart** adicional quando o usuário pressionar a tecla Listening.

O evento retorna o caractere para os clientes que atualmente têm esse caractere carregado. Todos os outros clientes recebem um caractere nulo (cadeia de caracteres vazia).

### <a name="see-also"></a>Consulte Também

[**Evento ListenComplete**](listencomplete-event.md), [ **método Listen**](listen-method.md)


 

 




