---
description: A semântica para contextos de datagramas ou sem conexão é ligeiramente diferente daquela para contextos orientados a conexão.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contextos de datagrama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090760"
---
# <a name="datagram-contexts"></a><span data-ttu-id="cd8d3-103">Contextos de datagrama</span><span class="sxs-lookup"><span data-stu-id="cd8d3-103">Datagram Contexts</span></span>

<span data-ttu-id="cd8d3-104">A semântica para contextos de [*datagramas*](/windows/desktop/SecGloss/d-gly)ou sem conexão é ligeiramente diferente daquela para contextos orientados a conexão.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-104">The semantics for [*datagram*](/windows/desktop/SecGloss/d-gly), or connectionless, contexts differ slightly from those for connection-oriented contexts.</span></span> <span data-ttu-id="cd8d3-105">No [*contexto*](/windows/desktop/SecGloss/c-gly)sem conexão de um datagrama, um servidor não pode determinar quando o cliente foi desligado ou, de outra forma, terminou a conexão.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-105">In a datagram's connectionless [*context*](/windows/desktop/SecGloss/c-gly), a server cannot determine when the client has shut down or otherwise terminated the connection.</span></span> <span data-ttu-id="cd8d3-106">Em outras palavras, nenhum aviso de encerramento é passado do aplicativo de transporte para o servidor, como ocorreria em um contexto orientado a conexão.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-106">In other words, no termination notice is passed from the transport application to the server as would occur in a connection-oriented context.</span></span>

<span data-ttu-id="cd8d3-107">Para usar um contexto de datagrama, um cliente define o \_ sinalizador de datagrama de req do ISC \_ em sua chamada para a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="cd8d3-107">To use a datagram context, a client sets the ISC\_REQ\_DATAGRAM flag in its call to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd8d3-108">O pacote [Kerberos da Microsoft](microsoft-kerberos.md) não oferece suporte a contextos de datagrama no modo de usuário para usuário.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-108">The [Microsoft Kerberos](microsoft-kerberos.md) package does not support datagram contexts in user-to-user mode.</span></span>

 

<span data-ttu-id="cd8d3-109">Para oferecer melhor suporte a alguns modelos, especialmente o RPC no estilo DCE, as seguintes regras se aplicam quando o cliente usa um contexto de datagrama:</span><span class="sxs-lookup"><span data-stu-id="cd8d3-109">To better support some models, particularly DCE-style RPC, the following rules apply when the client uses a datagram context:</span></span>

-   <span data-ttu-id="cd8d3-110">O [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) não produz um [*blob*](/windows/desktop/SecGloss/b-gly) de autenticação (objeto binário grande) na primeira chamada para [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="cd8d3-110">The [*security package*](/windows/desktop/SecGloss/s-gly) does not produce an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) (binary large object) on the first call to [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span> <span data-ttu-id="cd8d3-111">No entanto, o cliente pode usar o contexto de segurança retornado em uma chamada para a função [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para gerar uma assinatura para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-111">However, the client can use the returned security context in a call to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a signature for a message.</span></span>
-   <span data-ttu-id="cd8d3-112">O pacote de segurança deve permitir que o contexto seja restabelecido várias vezes para permitir que o servidor descarte a conexão sem aviso prévio.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-112">The security package must allow for the context to be re-established multiple times to allow the server to drop the connection without notice.</span></span> <span data-ttu-id="cd8d3-113">Isso implica que todas as chaves usadas nas funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) podem ser redefinidas para um [*estado*](/windows/desktop/SecGloss/s-gly)consistente.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-113">This implies that any keys used in the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions can be reset to a consistent [*state*](/windows/desktop/SecGloss/s-gly).</span></span>
-   <span data-ttu-id="cd8d3-114">O pacote de segurança permite que o chamador Especifique informações de sequência e forneça essas informações de sequência no lado do destinatário.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-114">The security package allows the caller to specify sequence information, and provides that sequence information at the receiver side.</span></span> <span data-ttu-id="cd8d3-115">Isso é além das informações de sequência mantidas pelo pacote.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-115">This is in addition to any sequence information maintained by the package.</span></span>

<span data-ttu-id="cd8d3-116">Um pacote de segurança define o \_ sinalizador de datagrama de sinalizador SECPKG \_ para indicar que ele dá suporte à semântica de datagrama.</span><span class="sxs-lookup"><span data-stu-id="cd8d3-116">A security package sets the SECPKG\_FLAG\_DATAGRAM flag to indicate that it supports datagram semantics.</span></span>

 

 
