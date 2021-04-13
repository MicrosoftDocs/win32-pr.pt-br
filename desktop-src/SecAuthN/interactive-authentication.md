---
description: A autenticação é interativa quando um usuário é solicitado a fornecer informações de logon. A autoridade de segurança local (LSA) executa uma autenticação interativa quando um usuário faz logon por meio da interface de usuário da GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticação interativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297261"
---
# <a name="interactive-authentication"></a><span data-ttu-id="99282-104">Autenticação interativa</span><span class="sxs-lookup"><span data-stu-id="99282-104">Interactive Authentication</span></span>

<span data-ttu-id="99282-105">A autenticação é interativa quando um usuário é solicitado a fornecer informações de logon.</span><span class="sxs-lookup"><span data-stu-id="99282-105">Authentication is interactive when a user is prompted to supply logon information.</span></span> <span data-ttu-id="99282-106">A [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) executa uma autenticação interativa quando um usuário faz logon por meio da interface de usuário da [*Gina*](../secgloss/g-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="99282-106">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) performs an interactive authentication when a user logs on through the [*GINA*](../secgloss/g-gly.md) user interface.</span></span> <span data-ttu-id="99282-107">A ilustração a seguir mostra as partes de uma autenticação interativa típica.</span><span class="sxs-lookup"><span data-stu-id="99282-107">The following illustration shows the parts of a typical interactive authentication.</span></span>

![autenticação interativa](images/lsaint3.png)

<span data-ttu-id="99282-109">Um usuário sinaliza o sistema para iniciar a sequência de logon digitando a SAS (sequência de [*atenção segura*](../secgloss/s-gly.md) ) Ctrl + Alt + Del.</span><span class="sxs-lookup"><span data-stu-id="99282-109">A user signals the system to begin the logon sequence by typing the CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS).</span></span> <span data-ttu-id="99282-110">O [*Winlogon*](../secgloss/w-gly.md) recebe a SAS e chama a Gina para exibir uma interface do usuário e obter os dados de logon do usuário, como um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="99282-110">[*Winlogon*](../secgloss/w-gly.md) receives the SAS and calls the GINA to display a user interface and obtain the user's logon data, such as a user name and password.</span></span>

<span data-ttu-id="99282-111">Depois de obter os dados de logon, o GINA chama a função [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) para autenticar o usuário, especificando qual pacote de autenticação deve ser usado para avaliar os dados de logon.</span><span class="sxs-lookup"><span data-stu-id="99282-111">After obtaining the logon data, the GINA calls the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) function to authenticate the user, specifying which authentication package must be used to evaluate the logon data.</span></span>

<span data-ttu-id="99282-112">O LSA chama o pacote de autenticação especificado e passa os dados de logon para ele.</span><span class="sxs-lookup"><span data-stu-id="99282-112">The LSA calls the specified authentication package and passes the logon data to it.</span></span> <span data-ttu-id="99282-113">O pacote de autenticação examina os dados e determina se a autenticação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="99282-113">The authentication package examines the data and determines whether the authentication is successful.</span></span> <span data-ttu-id="99282-114">O resultado da autenticação é retornado para a LSA e da LSA para a GINA.</span><span class="sxs-lookup"><span data-stu-id="99282-114">The authentication result is returned to the LSA and from the LSA, to the GINA.</span></span>

<span data-ttu-id="99282-115">A GINA exibe o êxito ou a falha da autenticação para o usuário e retorna o resultado da autenticação para o Winlogon.</span><span class="sxs-lookup"><span data-stu-id="99282-115">The GINA displays the success or failure of the authentication to the user and returns the result of the authentication to Winlogon.</span></span> <span data-ttu-id="99282-116">Se a autenticação for realizada com sucesso, a sessão de logon do usuário será iniciada e um conjunto de [*credenciais*](../secgloss/c-gly.md) de logon será salvo para referência futura.</span><span class="sxs-lookup"><span data-stu-id="99282-116">If the authentication succeeds, the user's logon session begins and a set of logon [*credentials*](../secgloss/c-gly.md) are saved for future reference.</span></span>

> [!Note]  
> <span data-ttu-id="99282-117">Em geral, um desenvolvedor que escreve uma GINA personalizada para aceitar dados de logon especializados, como um [*cartão inteligente*](../secgloss/s-gly.md) ou dados de retina, também deve escrever um pacote de autenticação responsável por processar esses dados e determinar sua autenticidade.</span><span class="sxs-lookup"><span data-stu-id="99282-117">In general, a developer who writes a custom GINA to accept specialized logon data, such as a [*smart card*](../secgloss/s-gly.md) or retinal-scan data, must also write an authentication package responsible for processing that data and determining its authenticity.</span></span>

 

<span data-ttu-id="99282-118">Para obter mais informações sobre Winlogon e GINAs, consulte [Winlogon e Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="99282-118">For more information about Winlogon and GINAs, see [Winlogon and GINA](winlogon-and-gina.md).</span></span> <span data-ttu-id="99282-119">Para obter mais informações sobre pacotes de autenticação, consulte [criando pacotes de segurança personalizados](creating-custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="99282-119">For more information about authentication packages, see [Creating Custom Security Packages](creating-custom-security-packages.md).</span></span>

 

 
