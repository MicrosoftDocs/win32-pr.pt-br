---
title: Propriedade de status
description: Propriedade de status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edb1196e5ec41571c9c760b91a72b350b94f6b85f1f85af018691d3f25ecec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245820"
---
# <a name="status-property"></a>Propriedade de status

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna o status do canal de saída de áudio.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent * * *. AudioOutput. status**



| Valor | Descrição                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | O canal de saída de áudio está disponível (não ocupado).                                                                 |
| 1     | Não há suporte para saída de áudio; por exemplo, como não há placa de som.                                |
| 2     | O canal de saída de áudio não pode ser aberto (está ocupado); por exemplo, como algum outro aplicativo está reproduzindo áudio. |
| 3     | O canal de saída de áudio está ocupado porque o servidor está processando a entrada de fala do usuário.                              |
| 4     | O canal de saída de áudio está ocupado porque um caractere está falando no momento.                                       |
| 5     | O canal de saída de áudio não está ocupado, mas está aguardando a entrada de fala do usuário.                                    |
| 6     | Houve algum outro problema (desconhecido) ao tentar acessar o canal de saída de áudio.                          |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa configuração permite que o aplicativo cliente consulte o canal de saída de áudio, retornando um valor inteiro que indica o status do canal de saída de áudio. Você pode usar isso para determinar se é apropriado que seu caractere fale ou se é apropriado tentar ativar o modo de escuta (usando o método [**Listen**](listen-method.md) ).

## <a name="see-also"></a>Consulte Também

[**Evento ListenComplete**](listencomplete-event.md)


 

 




