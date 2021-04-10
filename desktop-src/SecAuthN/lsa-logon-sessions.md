---
description: Uma sessão de logon é uma sessão de computação que começa quando uma autenticação de usuário é bem-sucedida e termina quando o usuário faz logoff do sistema.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sessões de logon LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170817"
---
# <a name="lsa-logon-sessions"></a><span data-ttu-id="bd6c4-103">Sessões de logon LSA</span><span class="sxs-lookup"><span data-stu-id="bd6c4-103">LSA Logon Sessions</span></span>

<span data-ttu-id="bd6c4-104">Uma [*sessão de logon*](../secgloss/l-gly.md) é uma sessão de computação que começa quando uma autenticação de usuário é bem-sucedida e termina quando o usuário faz logoff do sistema.</span><span class="sxs-lookup"><span data-stu-id="bd6c4-104">A [*logon session*](../secgloss/l-gly.md) is a computing session that begins when a user authentication is successful and ends when the user logs off of the system.</span></span>

<span data-ttu-id="bd6c4-105">Quando um usuário é autenticado com êxito, o pacote de autenticação cria uma sessão de logon e retorna informações para a LSA ( [*autoridade de segurança local*](../secgloss/l-gly.md) ) que é usada para criar um [*token*](../secgloss/t-gly.md) para o novo usuário.</span><span class="sxs-lookup"><span data-stu-id="bd6c4-105">When a user is successfully authenticated, the authentication package creates a logon session and returns information to the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) that is used to create a [*token*](../secgloss/t-gly.md) for the new user.</span></span> <span data-ttu-id="bd6c4-106">Esse token inclui, entre outras coisas, um [*identificador local exclusivo*](../secgloss/l-gly.md) (LUID) para a sessão de logon, chamado de [*ID de logon*](../secgloss/l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bd6c4-106">This token includes, among other things, a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) for the logon session, called the [*logon Id*](../secgloss/l-gly.md).</span></span>

<span data-ttu-id="bd6c4-107">Quando um token é criado, a [*contagem de referência*](../secgloss/r-gly.md) para a sessão de logon é incrementada.</span><span class="sxs-lookup"><span data-stu-id="bd6c4-107">When a token is created, the [*reference count*](../secgloss/r-gly.md) for the logon session is incremented.</span></span> <span data-ttu-id="bd6c4-108">A contagem de referência também é incrementada sempre que as cópias do token são criadas para a criação, representação ou outros usos do processo.</span><span class="sxs-lookup"><span data-stu-id="bd6c4-108">The reference count is also incremented whenever copies of the token are created for process creation, impersonation, or other uses.</span></span> <span data-ttu-id="bd6c4-109">Como os usos de token são concluídos e as cópias do token são excluídas, a contagem de referência para a sessão de logon é decrementada.</span><span class="sxs-lookup"><span data-stu-id="bd6c4-109">As token uses are completed and copies of the token are deleted, the reference count for the logon session is decremented.</span></span> <span data-ttu-id="bd6c4-110">Quando a contagem de referência chega a zero, a sessão de logon é excluída.</span><span class="sxs-lookup"><span data-stu-id="bd6c4-110">When the reference count reaches zero, the logon session is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="bd6c4-111">Se a autenticação não for bem-sucedida, o [*pacote de autenticação*](../secgloss/a-gly.md) não deverá criar uma sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="bd6c4-111">If authentication is not successful, the [*authentication package*](../secgloss/a-gly.md) should not create a logon session.</span></span> <span data-ttu-id="bd6c4-112">Se o pacote de autenticação precisar criar uma sessão de logon antes de fazer uma determinação final da validade do usuário e se a autenticação falhar, o pacote de autenticação deverá excluir a sessão.</span><span class="sxs-lookup"><span data-stu-id="bd6c4-112">If the authentication package must create a logon session before making a final determination about the validity of the user, and if authentication fails, the authentication package must delete the session.</span></span>

 

 

 
