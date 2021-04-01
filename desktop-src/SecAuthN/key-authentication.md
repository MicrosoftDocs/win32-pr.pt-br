---
description: Muitas formas de autenticação se baseiam na ideia de que uma entidade pode provar sua identidade se puder provar que ela conhece uma chave, como uma senha, que só pode ser conhecida.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticação de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169828"
---
# <a name="key-authentication"></a><span data-ttu-id="31d75-103">Autenticação de chave</span><span class="sxs-lookup"><span data-stu-id="31d75-103">Key Authentication</span></span>

<span data-ttu-id="31d75-104">Muitas formas de autenticação se baseiam na ideia de que uma entidade pode provar sua identidade se puder provar que ela conhece uma chave, como uma senha, que só pode ser conhecida.</span><span class="sxs-lookup"><span data-stu-id="31d75-104">Many forms of authentication are based on the idea that an entity can prove its identity if it can prove it knows a key, such as a password, that only it can know.</span></span>

<span data-ttu-id="31d75-105">As técnicas de autenticação que dependem de um segredo, como uma senha, precisam ter uma maneira de manter o segredo de se tornarem um conhecimento público.</span><span class="sxs-lookup"><span data-stu-id="31d75-105">Authentication techniques that rely on a secret, such as a password, need to have a way to keep the secret from becoming public knowledge.</span></span> <span data-ttu-id="31d75-106">Um proprietário de senha não pode ir até uma porta e fornecer a senha.</span><span class="sxs-lookup"><span data-stu-id="31d75-106">A password owner cannot walk up to a door and give the password.</span></span> <span data-ttu-id="31d75-107">Alguém além do doorkeeper pode estar ouvindo; ou pode ser a porta errada.</span><span class="sxs-lookup"><span data-stu-id="31d75-107">Someone besides the doorkeeper might be listening; or it might be the wrong door.</span></span> <span data-ttu-id="31d75-108">Para manter um segredo, deve haver uma maneira de provar que um usuário sabe a senha sem revelar a senha.</span><span class="sxs-lookup"><span data-stu-id="31d75-108">In order to keep a secret, there must be a way to prove a user knows the password without revealing the password.</span></span> <span data-ttu-id="31d75-109">Essa é a ideia por trás da autenticação de chave secreta, um método de verificação usado em todo o [*protocolo Kerberos*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="31d75-109">That is the idea behind secret key authentication, a method of verification used throughout the [*Kerberos protocol*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="31d75-110">Observe que o "segredo" na autenticação de chave secreta é que o processo de autenticação ocorre "em segredo"; ou seja, sem jamais revelar o conteúdo da chave.</span><span class="sxs-lookup"><span data-stu-id="31d75-110">Notice that the "secret" in secret key authentication is that the authentication process takes place "in secret;" that is, without ever actually revealing the content of the key.</span></span>

<span data-ttu-id="31d75-111">Para que a autenticação de chave secreta funcione, as duas partes de uma transação devem compartilhar uma [*chave de sessão*](../secgloss/s-gly.md) criptográfica que também é secreta, conhecida apenas para elas e para nenhuma outra.</span><span class="sxs-lookup"><span data-stu-id="31d75-111">For secret key authentication to work, the two parties to a transaction must share a cryptographic [*session key*](../secgloss/s-gly.md) which is also secret, known only to them and to no others.</span></span> <span data-ttu-id="31d75-112">A chave é [*simétrica*](../secgloss/s-gly.md); ou seja, é uma chave única usada para criptografia e descriptografia.</span><span class="sxs-lookup"><span data-stu-id="31d75-112">The key is [*symmetric*](../secgloss/s-gly.md); that is, it is a single key used for both encryption and decryption.</span></span> <span data-ttu-id="31d75-113">Uma das partes no processo de autenticação comprova seu conhecimento da chave criptografando uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="31d75-113">One party in the authentication process proves its knowledge of the key by encrypting a message.</span></span> <span data-ttu-id="31d75-114">A outra parte comprova seu conhecimento da chave descriptografando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="31d75-114">The other party proves its knowledge of the key by decrypting the message.</span></span>

 

 
