---
description: O modelo de segurança usado no protocolo SMB da Microsoft é idêntico ao usado por outras variantes de SMB e consiste em dois níveis de segurança&\# 8212; usuário e compartilhamento.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Autenticação do protocolo SMB da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827065"
---
# <a name="microsoft-smb-protocol-authentication"></a><span data-ttu-id="a5cc1-103">Autenticação do protocolo SMB da Microsoft</span><span class="sxs-lookup"><span data-stu-id="a5cc1-103">Microsoft SMB Protocol Authentication</span></span>

<span data-ttu-id="a5cc1-104">O modelo de segurança usado no protocolo SMB da Microsoft é idêntico ao usado por outras variantes de SMB e consiste em dois níveis de segurança: usuário e compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-104">The security model used in Microsoft SMB Protocol is identical to the one used by other variants of SMB, and consists of two levels of security—user and share.</span></span> <span data-ttu-id="a5cc1-105">Um compartilhamento é um arquivo, diretório ou impressora que pode ser acessado pelos clientes do protocolo Microsoft SMB.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-105">A share is a file, directory, or printer that can be accessed by Microsoft SMB Protocol clients.</span></span>

<span data-ttu-id="a5cc1-106">A autenticação no nível do usuário indica que o cliente que está tentando acessar um compartilhamento em um servidor deve fornecer um nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-106">User-level authentication indicates that the client attempting to access a share on a server must provide a user name and password.</span></span> <span data-ttu-id="a5cc1-107">Quando autenticado, o usuário pode acessar todos os compartilhamentos em um servidor também não protegido pela segurança em nível de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-107">When authenticated, the user can then access all shares on a server not also protected by share-level security.</span></span> <span data-ttu-id="a5cc1-108">Esse nível de segurança permite que os administradores do sistema determinem especificamente quais usuários e grupos podem acessar um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-108">This security level allows system administrators to specifically determine which users and groups can access a share.</span></span>

<span data-ttu-id="a5cc1-109">A autenticação de nível de compartilhamento indica que o acesso a um compartilhamento é controlado por uma senha atribuída somente a esse compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-109">Share-level authentication indicates that access to a share is controlled by a password assigned to that share only.</span></span> <span data-ttu-id="a5cc1-110">Diferentemente da segurança em nível de usuário, esse nível de segurança não exige um nome de usuário para autenticação e nenhuma identidade de usuário é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-110">Unlike user-level security, this security level does not require a user name for authentication and no user identity is established.</span></span>

<span data-ttu-id="a5cc1-111">Em ambos os níveis de segurança, a senha é criptografada antes de ser enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-111">Under both of these security levels, the password is encrypted before it is sent to the server.</span></span> <span data-ttu-id="a5cc1-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) e a criptografia do LM (LAN Manager) mais antiga têm suporte pelo protocolo SMB da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) and the older LAN Manager (LM) encryption are supported by Microsoft SMB Protocol.</span></span> <span data-ttu-id="a5cc1-113">Os dois métodos de criptografia usam a autenticação de desafio/resposta, em que o servidor envia ao cliente uma cadeia de caracteres aleatória e o cliente retorna uma cadeia de caracteres de resposta computada que comprova que o cliente tem credenciais suficientes para acesso.</span><span class="sxs-lookup"><span data-stu-id="a5cc1-113">Both encryption methods use challenge-response authentication, where the server sends the client a random string and the client returns a computed response string that proves the client has sufficient credentials for access.</span></span>

 

 
