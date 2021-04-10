---
description: O protocolo CredSSP é um provedor de suporte de segurança que é implementado usando a interface de provedor de suporte de segurança (SSPI).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Provedor de suporte à segurança de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164868"
---
# <a name="credential-security-support-provider"></a><span data-ttu-id="a137f-103">Provedor de suporte à segurança de credenciais</span><span class="sxs-lookup"><span data-stu-id="a137f-103">Credential Security Support Provider</span></span>

<span data-ttu-id="a137f-104">O protocolo CredSSP é um provedor de suporte de segurança que é implementado usando a interface de provedor de suporte de segurança ([SSPI](sspi.md)).</span><span class="sxs-lookup"><span data-stu-id="a137f-104">The Credential Security Support Provider protocol (CredSSP) is a Security Support Provider that is implemented by using the Security Support Provider Interface ([SSPI](sspi.md)).</span></span> <span data-ttu-id="a137f-105">O CredSSP permite que um aplicativo delegue as credenciais do usuário do cliente para o servidor de destino para autenticação remota.</span><span class="sxs-lookup"><span data-stu-id="a137f-105">CredSSP lets an application delegate the user's credentials from the client to the target server for remote authentication.</span></span> <span data-ttu-id="a137f-106">O CredSSP fornece um canal de [protocolo de segurança de camada de transporte](transport-layer-security-protocol.md) criptografado.</span><span class="sxs-lookup"><span data-stu-id="a137f-106">CredSSP provides an encrypted [Transport Layer Security Protocol](transport-layer-security-protocol.md) channel.</span></span> <span data-ttu-id="a137f-107">O cliente é autenticado pelo canal criptografado usando o protocolo Negotiate (SPNEGO) simples e protegido com o [Microsoft Kerberos](microsoft-kerberos.md) ou o [Microsoft NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="a137f-107">The client is authenticated over the encrypted channel by using the Simple and Protected Negotiate (SPNEGO) protocol with either [Microsoft Kerberos](microsoft-kerberos.md) or [Microsoft NTLM](microsoft-ntlm.md).</span></span>

> [!Caution]  
> <span data-ttu-id="a137f-108">Essa não é uma delegação restrita.</span><span class="sxs-lookup"><span data-stu-id="a137f-108">This is not constrained delegation.</span></span> <span data-ttu-id="a137f-109">O CredSSP passa as credenciais completas do usuário para o servidor sem nenhuma restrição.</span><span class="sxs-lookup"><span data-stu-id="a137f-109">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="a137f-110">Para obter informações sobre o SPNEGO, consulte [Microsoft Negotiate](microsoft-negotiate.md).</span><span class="sxs-lookup"><span data-stu-id="a137f-110">For information about SPNEGO, see [Microsoft Negotiate](microsoft-negotiate.md).</span></span>

<span data-ttu-id="a137f-111">Depois que o cliente e o servidor são autenticados, o cliente passa as credenciais do usuário para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a137f-111">After the client and server are authenticated, the client passes the user's credentials to the server.</span></span> <span data-ttu-id="a137f-112">As credenciais são criptografadas duplamente nas chaves de sessão SPNEGO e TLS.</span><span class="sxs-lookup"><span data-stu-id="a137f-112">The credentials are doubly encrypted under the SPNEGO and TLS session keys.</span></span> <span data-ttu-id="a137f-113">O CredSSP dá suporte ao logon baseado em senha, bem como ao logon de cartão inteligente com base em [*X. 509*](/windows/desktop/SecGloss/x-gly) e PKINIT.</span><span class="sxs-lookup"><span data-stu-id="a137f-113">CredSSP supports password-based logon as well as smart card logon based on both [*X.509*](/windows/desktop/SecGloss/x-gly) and PKINIT.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a137f-114">O CredSSP não dá suporte a clientes WOW64.</span><span class="sxs-lookup"><span data-stu-id="a137f-114">CredSSP does not support Wow64 clients.</span></span>

 

<span data-ttu-id="a137f-115">Para obter mais informações sobre CredSSP, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a137f-115">For more information about CredSSP, see the following topics.</span></span>



| <span data-ttu-id="a137f-116">Tópico</span><span class="sxs-lookup"><span data-stu-id="a137f-116">Topic</span></span>                                                                         | <span data-ttu-id="a137f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="a137f-117">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a137f-118">Configurações de Política de Grupo CredSSP</span><span class="sxs-lookup"><span data-stu-id="a137f-118">CredSSP Group Policy Settings</span></span>](credssp-group-policy-settings.md)<br/> | <span data-ttu-id="a137f-119">A delegação de credenciais por CredSSP pode ser controlada usando configurações de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="a137f-119">Delegation of credentials by CredSSP can be controlled by using group policy settings.</span></span><br/> |



 

 

