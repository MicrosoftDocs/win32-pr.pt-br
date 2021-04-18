---
description: Para alterar os atributos de uma conexão, como o pacote de codificação ou a autenticação de cliente, você pode solicitar um &\# 0034; refazer&\# 0034; ou renegociar a conexão.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Renegociar uma conexão Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751819"
---
# <a name="renegotiating-an-schannel-connection"></a><span data-ttu-id="15a55-103">Renegociar uma conexão Schannel</span><span class="sxs-lookup"><span data-stu-id="15a55-103">Renegotiating an Schannel Connection</span></span>

<span data-ttu-id="15a55-104">Para alterar os atributos de uma conexão, como o pacote de codificação ou a autenticação de cliente, você pode solicitar uma "refazer" ou renegociar a conexão.</span><span class="sxs-lookup"><span data-stu-id="15a55-104">To change a connection's attributes, such as the cipher suite or client authentication, you can request a "redo" or renegotiation of the connection.</span></span>

<span data-ttu-id="15a55-105">Se os atributos que você deseja alterar forem controlados por credenciais, você deverá obter novas credenciais antes de renegociar a conexão.</span><span class="sxs-lookup"><span data-stu-id="15a55-105">If the attributes you want to change are controlled by credentials, you must obtain new credentials before you renegotiate the connection.</span></span> <span data-ttu-id="15a55-106">Para obter mais informações, consulte [obtendo credenciais Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="15a55-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

<span data-ttu-id="15a55-107">Para solicitar uma refazer de um aplicativo cliente, chame a função [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="15a55-107">To request a redo from a client application, call the [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="15a55-108">Os aplicativos de servidor chamam a função [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="15a55-108">Server applications call the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="15a55-109">Defina os parâmetros da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="15a55-109">Set the parameters as follows:</span></span>

-   <span data-ttu-id="15a55-110">Especifique o [*contexto de segurança*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) existente no parâmetro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="15a55-110">Specify the existing [*security context*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) in the *phContext* parameter.</span></span>
-   <span data-ttu-id="15a55-111">(Somente clientes) Especifique o mesmo nome de servidor (no parâmetro *pszTargetName* ) conforme especificado ao estabelecer o contexto.</span><span class="sxs-lookup"><span data-stu-id="15a55-111">(Clients only) Specify the same server name (in the *pszTargetName* parameter) as specified when establishing the context.</span></span>
-   <span data-ttu-id="15a55-112">Especifique novas credenciais, usando o parâmetro *phCredential* , se aplicável.</span><span class="sxs-lookup"><span data-stu-id="15a55-112">Specify new credentials, using the *phCredential* parameter, if applicable.</span></span>
-   <span data-ttu-id="15a55-113">Se você quiser alterar atributos de contexto não relacionados às credenciais, especifique esses atributos usando o parâmetro *fContextReq* .</span><span class="sxs-lookup"><span data-stu-id="15a55-113">If you want to change context attributes unrelated to the credentials, specify these attributes using the *fContextReq* parameter.</span></span>

<span data-ttu-id="15a55-114">Depois de chamar a função apropriada, seu aplicativo deve enviar os resultados para o cliente e continuar processando mensagens de entrada usando a função [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="15a55-114">After calling the appropriate function, your application should send the results to the client and continue processing incoming messages using the [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function.</span></span>

<span data-ttu-id="15a55-115">A função [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) retornará SEC \_ que \_ renegociará quando o Schannel estiver pronto para o aplicativo continuar.</span><span class="sxs-lookup"><span data-stu-id="15a55-115">The [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function will return SEC\_I\_RENEGOTIATE when Schannel is ready for your application to proceed.</span></span> <span data-ttu-id="15a55-116">Quando você recebe o \_ código de retorno s I \_ renegotiate, seu aplicativo deve chamar [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (servidores) ou [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clientes) e passar o conteúdo de SECBUFFER_EXTRA retornado de DecryptMessage no SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="15a55-116">When you receive the SEC\_I\_RENEGOTIATE return code, your application must call [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (servers) or [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clients), and pass the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="15a55-117">Depois que essa chamada retornar um valor, prossiga como se seu aplicativo estivesse criando uma nova conexão.</span><span class="sxs-lookup"><span data-stu-id="15a55-117">After this call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 
