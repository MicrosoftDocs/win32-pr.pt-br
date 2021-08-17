---
title: Evento ListenComplete
description: Evento ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d25e9bfbf23c6a2911c718b576c99395ef06fd802853b39b699384a9ab92429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883888"
---
# <a name="listencomplete-event"></a>Evento ListenComplete

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o modo de escuta (reconhecimento de fala) termina.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent. * * * ListenComplete (ByVal* *  *characterid*, **ByVal** *causa * * *)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere de escuta como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Causa*       | Retorna a causa do evento complete como um inteiro que pode ser um dos seguintes: 1 modo de escuta foi desativado pelo código do programa.<br/> 2 o modo de escuta (ativado pelo código do programa) atingiu o tempo limite.<br/> 3 o modo de escuta (ativado pela chave de escuta) atingiu o tempo limite.<br/> 4 o modo de escuta foi desativado porque o usuário liberou a chave de escuta.<br/> 5 o modo de escuta terminou porque o usuário terminou de falar.<br/> 6 o modo de escuta foi encerrado porque o cliente de entrada-ativo foi desativado.<br/> 7 modo de escuta encerrado porque o caractere padrão foi alterado.<br/> 8 modo de escuta terminou porque o usuário desabilitou a entrada de fala.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento é enviado a todos os clientes quando o tempo limite do modo de escuta termina, depois que o usuário libera a chave de escuta, quando o cliente ativo de entrada chama o método [**Listen**](listen-method.md) com **false** ou o usuário terminou de falar. Você pode usar esse evento para determinar quando retomar a saída de caractere falado (áudio).

Se você ativar o modo de escuta usando o método [**Listen**](listen-method.md) e, em seguida, o usuário pressionar a tecla de escuta, o modo de escuta redefinirá e continuará até que o tempo limite da chave de escuta seja concluído, a chave de escuta será liberada ou o usuário terminará de falar, o que for mais tarde. Nessa situação, você não receberá um evento **ListenComplete** até que o modo da chave de escuta seja concluído.

O evento retorna o caractere para os clientes que atualmente têm esse caractere carregado. Todos os outros clientes recebem um caractere nulo (cadeia de caracteres vazia).

### <a name="see-also"></a>Consulte Também

[**Evento ListenStart**](listenstart-event.md), [ **método Listen**](listen-method.md)


 

 





