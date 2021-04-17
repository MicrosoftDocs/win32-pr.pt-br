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
# <a name="sspi-context-semantics"></a><span data-ttu-id="38082-103">Semântica de contexto SSPI</span><span class="sxs-lookup"><span data-stu-id="38082-103">SSPI Context Semantics</span></span>

<span data-ttu-id="38082-104">Um [*contexto de segurança*](../secgloss/s-gly.md) é o conjunto de regras e atributos de segurança em vigor durante uma sessão de comunicação.</span><span class="sxs-lookup"><span data-stu-id="38082-104">A [*security context*](../secgloss/s-gly.md) is the set of security attributes and rules in effect during a communication session.</span></span> <span data-ttu-id="38082-105">Isso inclui informações como as identidades da entidade de segurança e as informações sobre as chaves, codificações e algoritmos que estão sendo usados.</span><span class="sxs-lookup"><span data-stu-id="38082-105">This includes such information as the identities of the principal and information on the keys, ciphers, and algorithms being used.</span></span> <span data-ttu-id="38082-106">Para a SSPI ( [*interface do provedor de suporte de segurança*](../secgloss/s-gly.md) ), um contexto de segurança é uma estrutura opaca que é criada por meio de uma troca que envolve a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e a função [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .</span><span class="sxs-lookup"><span data-stu-id="38082-106">For [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), a security context is an opaque structure that is created through an exchange involving the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function and the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>

<span data-ttu-id="38082-107">Para obter mais informações sobre os atributos de contexto, consulte [requisitos de contexto](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="38082-107">For more information about the context attributes, see [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="38082-108">O modelo SSPI dá suporte a três tipos de contextos de segurança.</span><span class="sxs-lookup"><span data-stu-id="38082-108">The SSPI model supports three types of security contexts.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38082-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="38082-109">Type</span></span></th>
<th><span data-ttu-id="38082-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="38082-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38082-111"><a href="connection-oriented-contexts.md">Conexão</a></span><span class="sxs-lookup"><span data-stu-id="38082-111"><a href="connection-oriented-contexts.md">Connection</a></span></span></td>
<td><span data-ttu-id="38082-112">Um <a href="/windows/desktop/SecGloss/c-gly"><em>contexto</em></a> orientado a conexão é o contexto de segurança mais comum e o mais simples de usar.</span><span class="sxs-lookup"><span data-stu-id="38082-112">A connection-oriented <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> is the most common security context, and the simplest to use.</span></span> <span data-ttu-id="38082-113">O chamador é responsável pelo formato de mensagem geral e pelo local dos dados na mensagem.</span><span class="sxs-lookup"><span data-stu-id="38082-113">The caller is responsible for the overall message format and for the location of the data in the message.</span></span> <span data-ttu-id="38082-114">O chamador também é responsável pelo local dos campos relevantes de segurança dentro de uma mensagem, como o local dos dados de assinatura.</span><span class="sxs-lookup"><span data-stu-id="38082-114">The caller is also responsible for the location of the security-relevant fields within a message, such as the location of the signature data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38082-115"><a href="datagram-contexts.md">Datagrama</a></span><span class="sxs-lookup"><span data-stu-id="38082-115"><a href="datagram-contexts.md">Datagram</a></span></span></td>
<td><span data-ttu-id="38082-116">Um contexto orientado a <a href="/windows/desktop/SecGloss/d-gly"><em>datagrama</em></a>tem suporte extra para comunicação de datagrama de estilo DCE.</span><span class="sxs-lookup"><span data-stu-id="38082-116">A <a href="/windows/desktop/SecGloss/d-gly"><em>datagram</em></a>-oriented context has extra support for DCE-style datagram communication.</span></span> <span data-ttu-id="38082-117">Ele também pode ser usado genericamente para um aplicativo de transporte orientado por datagrama.</span><span class="sxs-lookup"><span data-stu-id="38082-117">It can also be used generically for a datagram-oriented transport application.</span></span><br/>
<blockquote>
<p>[!Important]</p>
<p><span data-ttu-id="38082-118">O pacote <a href="microsoft-kerberos.md">Kerberos da Microsoft</a> não oferece suporte a contextos de datagrama no modo de usuário para usuário.</span><span class="sxs-lookup"><span data-stu-id="38082-118">The <a href="microsoft-kerberos.md">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38082-119"><a href="stream-contexts.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="38082-119"><a href="stream-contexts.md">Stream</a></span></span></td>
<td><span data-ttu-id="38082-120">Um contexto orientado a fluxo é responsável pelo bloqueio e pela formatação da mensagem no pacote de segurança.</span><span class="sxs-lookup"><span data-stu-id="38082-120">A stream-oriented context is responsible for the blocking and message formatting within the security package.</span></span> <span data-ttu-id="38082-121">O chamador não está interessado em formatação, mas sim um fluxo de dados bruto.</span><span class="sxs-lookup"><span data-stu-id="38082-121">The caller is not interested in formatting, but rather a raw stream of data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="38082-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38082-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38082-123">Requisitos de contexto</span><span class="sxs-lookup"><span data-stu-id="38082-123">Context Requirements</span></span>](context-requirements.md)
</dt> <dt>

[<span data-ttu-id="38082-124">Contextos orientados a conexão</span><span class="sxs-lookup"><span data-stu-id="38082-124">Connection-Oriented Contexts</span></span>](connection-oriented-contexts.md)
</dt> <dt>

[<span data-ttu-id="38082-125">Contextos de datagrama</span><span class="sxs-lookup"><span data-stu-id="38082-125">Datagram Contexts</span></span>](datagram-contexts.md)
</dt> <dt>

[<span data-ttu-id="38082-126">Contextos de fluxo</span><span class="sxs-lookup"><span data-stu-id="38082-126">Stream Contexts</span></span>](stream-contexts.md)
</dt> </dl>

 

 
