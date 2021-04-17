---
description: Um contexto de segurança é o conjunto de regras e atributos de segurança em vigor durante uma sessão de comunicação.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semântica de contexto SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752825"
---
# <a name="sspi-context-semantics"></a>Semântica de contexto SSPI

Um [*contexto de segurança*](../secgloss/s-gly.md) é o conjunto de regras e atributos de segurança em vigor durante uma sessão de comunicação. Isso inclui informações como as identidades da entidade de segurança e as informações sobre as chaves, codificações e algoritmos que estão sendo usados. Para a SSPI ( [*interface do provedor de suporte de segurança*](../secgloss/s-gly.md) ), um contexto de segurança é uma estrutura opaca que é criada por meio de uma troca que envolve a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e a função [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .

Para obter mais informações sobre os atributos de contexto, consulte [requisitos de contexto](context-requirements.md).

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
<td>Um <a href="/windows/desktop/SecGloss/c-gly"><em>contexto</em></a> orientado a conexão é o contexto de segurança mais comum e o mais simples de usar. O chamador é responsável pelo formato de mensagem geral e pelo local dos dados na mensagem. O chamador também é responsável pelo local dos campos relevantes de segurança dentro de uma mensagem, como o local dos dados de assinatura.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagrama</a></td>
<td>Um contexto orientado a <a href="/windows/desktop/SecGloss/d-gly"><em>datagrama</em></a>tem suporte extra para comunicação de datagrama de estilo DCE. Ele também pode ser usado genericamente para um aplicativo de transporte orientado por datagrama.<br/>
<blockquote>
<p>[!Important]</p>
<p>O pacote <a href="microsoft-kerberos.md">Kerberos da Microsoft</a> não oferece suporte a contextos de datagrama no modo de usuário para usuário.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Stream</a></td>
<td>Um contexto orientado a fluxo é responsável pelo bloqueio e pela formatação da mensagem no pacote de segurança. O chamador não está interessado em formatação, mas sim um fluxo de dados bruto.<br/></td>
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

 

 
