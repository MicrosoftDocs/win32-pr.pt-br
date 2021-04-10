---
description: O pacote de autenticação Kerberos é usado ao fazer logon em uma rede; os logons locais são tratados por MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: SSP/PA Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011143"
---
# <a name="kerberos-sspap"></a><span data-ttu-id="67e60-103">SSP/PA Kerberos</span><span class="sxs-lookup"><span data-stu-id="67e60-103">Kerberos SSP/AP</span></span>

<span data-ttu-id="67e60-104">O pacote de autenticação [*Kerberos*](../secgloss/k-gly.md) é usado ao fazer logon em uma rede; os logons locais são tratados por MSV1 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="67e60-104">The [*Kerberos*](../secgloss/k-gly.md) authentication package is used when logging on to a network; local logons are handled by MSV1\_0.</span></span>

<span data-ttu-id="67e60-105">Quando um usuário faz logon usando uma conta de rede, por padrão, o Kerberos tenta se conectar ao [*centro de distribuição de chaves*](../secgloss/k-gly.md) do Kerberos (KDC) no controlador de domínio e obter um tíquete de concessão de TÍQUETE (TGT) usando os dados de logon fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="67e60-105">When a user logs on using a network account, by default, Kerberos attempts to connect to the Kerberos [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) on the domain controller and obtain a ticket granting ticket (TGT) by using the logon data supplied by the user.</span></span>

<span data-ttu-id="67e60-106">Se um KDC Kerberos não estiver disponível, o Windows usará \_ o MSV1 0 e a autenticação de passagem, conforme descrito no [pacote de autenticação do MSV1 \_ 0](msv1-0-authentication-package.md).</span><span class="sxs-lookup"><span data-stu-id="67e60-106">If a Kerberos KDC is not available, Windows uses MSV1\_0 and pass-through authentication as described in [MSV1\_0 Authentication Package](msv1-0-authentication-package.md).</span></span>

<span data-ttu-id="67e60-107">O pacote de autenticação Kerberos dá suporte à versão 5, revisão 6 do protocolo Kerberos.</span><span class="sxs-lookup"><span data-stu-id="67e60-107">The Kerberos authentication package supports version 5, revision 6 of the Kerberos protocol.</span></span> <span data-ttu-id="67e60-108">Esse protocolo é baseado no [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)da Internet.</span><span class="sxs-lookup"><span data-stu-id="67e60-108">This protocol is based on Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span></span> <span data-ttu-id="67e60-109">Para obter mais informações, consulte o site da IETF:</span><span class="sxs-lookup"><span data-stu-id="67e60-109">For more information, see the IETF website:</span></span>

[https://www.ietf.org](https://www.ietf.org/)

<span data-ttu-id="67e60-110">Para obter mais informações sobre o Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="67e60-110">For more information about Kerberos, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

## <a name="kerberos-credential-formats"></a><span data-ttu-id="67e60-111">Formatos de credencial Kerberos</span><span class="sxs-lookup"><span data-stu-id="67e60-111">Kerberos Credential Formats</span></span>

<span data-ttu-id="67e60-112">As [*credenciais*](../secgloss/c-gly.md) de usuário atribuídas pelo pacote de autenticação Kerberos após uma tentativa de logon bem-sucedida são um tíquete e uma chave de criptografia temporária, geralmente chamada de [*chave de sessão*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="67e60-112">The user [*credentials*](../secgloss/c-gly.md) assigned by the Kerberos authentication package after a successful logon attempt are a ticket and a temporary encryption key, often called a [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="67e60-113">O tíquete contém uma cópia criptografada das credenciais do cliente e da chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="67e60-113">The ticket contains both an encrypted copy of the client's credentials and the session key.</span></span>

 

 
