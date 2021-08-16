---
description: Um contexto de segurança é o conjunto de atributos de segurança e regras em vigor durante uma sessão de comunicação.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semântica de contexto SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddadd2c8a76f1fdc151273dca2027b8cb55776a50b78a7c08343c22410ae90e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916975"
---
# <a name="sspi-context-semantics"></a>Semântica de contexto SSPI

Um [*contexto de segurança*](../secgloss/s-gly.md) é o conjunto de atributos de segurança e regras em vigor durante uma sessão de comunicação. Isso inclui informações como as identidades da entidade de segurança e informações sobre as chaves, as codificações e os algoritmos que estão sendo usados. Para a [*SSPI (Interface*](../secgloss/s-gly.md) do Provedor de Suporte de Segurança), um contexto de segurança é uma estrutura opaca criada por meio de uma troca que envolve a função [**InitializeSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e a [**função AcceptSecurityContext (Geral).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

Para obter mais informações sobre os atributos de contexto, consulte [Context Requirements](context-requirements.md).

O modelo SSPI dá suporte a três tipos de contextos de segurança.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="connection-oriented-contexts.md">Conexão</a></td>
<td>Um contexto orientado a <a href="/windows/desktop/SecGloss/c-gly"><em>conexão</em></a> é o contexto de segurança mais comum e o mais simples de usar. O chamador é responsável pelo formato geral da mensagem e pelo local dos dados na mensagem. O chamador também é responsável pela localização dos campos relevantes para a segurança dentro de uma mensagem, como o local dos dados de assinatura.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagrama</a></td>
<td>Um <a href="/windows/desktop/SecGloss/d-gly"><em>contexto orientado a datagrama</em></a>tem suporte extra para comunicação de datagrama no estilo DCE. Ele também pode ser usado genericamente para um aplicativo de transporte orientado a datagrama.<br/>
<blockquote>
<p>[!Important]</p>
<p>O <a href="microsoft-kerberos.md">pacote Microsoft Kerberos</a> não dá suporte a contextos de datagrama no modo de usuário para usuário.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Fluxo</a></td>
<td>Um contexto orientado a fluxo é responsável pelo bloqueio e pela formatação de mensagens dentro do pacote de segurança. O chamador não está interessado em formatação, mas em um fluxo bruto de dados.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Requisitos de contexto](context-requirements.md)
</dt> <dt>

[Contextos orientados a conexão](connection-oriented-contexts.md)
</dt> <dt>

[Contextos de datagrama](datagram-contexts.md)
</dt> <dt>

[Contextos de fluxo](stream-contexts.md)
</dt> </dl>

 

 
