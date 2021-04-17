---
title: Criando uma nova conta de computador
description: O exemplo de código a seguir demonstra como criar uma nova conta de computador usando a função NetUserAdd.
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd02a9d2053310c50e40957e6afee6e3a4a5ab1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105775677"
---
# <a name="creating-a-new-computer-account"></a><span data-ttu-id="2d2ab-103">Criando uma nova conta de computador</span><span class="sxs-lookup"><span data-stu-id="2d2ab-103">Creating a New Computer Account</span></span>

<span data-ttu-id="2d2ab-104">O exemplo de código a seguir demonstra como criar uma nova conta de computador usando a função [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .</span><span class="sxs-lookup"><span data-stu-id="2d2ab-104">The following code sample demonstrates how to create a new computer account using the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) function.</span></span>

<span data-ttu-id="2d2ab-105">Veja a seguir as considerações para o gerenciamento de contas de computador:</span><span class="sxs-lookup"><span data-stu-id="2d2ab-105">The following are considerations for managing computer accounts:</span></span>

-   <span data-ttu-id="2d2ab-106">O nome da conta do computador deve estar em letras maiúsculas para fins de consistência com os utilitários de gerenciamento de conta.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-106">The computer account name should be all uppercase for consistency with account management utilities.</span></span>
-   <span data-ttu-id="2d2ab-107">Um nome de conta de computador sempre tem um sinal de dólar à direita ($).</span><span class="sxs-lookup"><span data-stu-id="2d2ab-107">A computer account name always has a trailing dollar sign ($).</span></span> <span data-ttu-id="2d2ab-108">Todas as funções usadas para gerenciar contas de computador devem criar o nome do computador de modo que o último caractere do nome da conta de computador seja um cifrão ($).</span><span class="sxs-lookup"><span data-stu-id="2d2ab-108">Any functions used to manage computer accounts must build the computer name such that the last character of the computer account name is a dollar sign ($).</span></span> <span data-ttu-id="2d2ab-109">Para relação de confiança entre domínios, o nome da conta é TrustingDomainName $.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-109">For interdomain trust, the account name is TrustingDomainName$.</span></span>
-   <span data-ttu-id="2d2ab-110">O comprimento máximo do nome do computador é o \_ \_ comprimento máximo de ComputerName (15).</span><span class="sxs-lookup"><span data-stu-id="2d2ab-110">The maximum computer name length is MAX\_COMPUTERNAME\_LENGTH (15).</span></span> <span data-ttu-id="2d2ab-111">Esse comprimento não inclui o sinal de dólar à direita ($).</span><span class="sxs-lookup"><span data-stu-id="2d2ab-111">This length does not include the trailing dollar sign ($).</span></span>
-   <span data-ttu-id="2d2ab-112">A senha para uma nova conta de computador deve ser a representação em minúsculas do nome da conta do computador, sem o sinal de dólar à direita ($).</span><span class="sxs-lookup"><span data-stu-id="2d2ab-112">The password for a new computer account should be the lowercase representation of the computer account name, without the trailing dollar sign ($).</span></span> <span data-ttu-id="2d2ab-113">Para relação de confiança entre domínios, a senha pode ser um valor arbitrário que corresponde ao valor especificado no lado de confiança da relação.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-113">For interdomain trust, the password can be an arbitrary value that matches the value specified on the trust side of the relationship.</span></span>
-   <span data-ttu-id="2d2ab-114">O comprimento máximo da senha é LM20 \_ PWLEN (14).</span><span class="sxs-lookup"><span data-stu-id="2d2ab-114">The maximum password length is LM20\_PWLEN (14).</span></span> <span data-ttu-id="2d2ab-115">A senha deve ser truncada para esse comprimento se o nome da conta do computador exceder esse comprimento.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-115">The password should be truncated to this length if the computer account name exceeds this length.</span></span>
-   <span data-ttu-id="2d2ab-116">A senha fornecida em hora da criação da conta de computador é válida somente até que a conta de computador se torne ativa no domínio.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-116">The password provided at computer-account-creation time is valid only until the computer account becomes active on the domain.</span></span> <span data-ttu-id="2d2ab-117">Uma nova senha é estabelecida durante a ativação da relação de confiança.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-117">A new password is established during trust relationship activation.</span></span>


```C++
#include <windows.h>
#include <lm.h>
#pragma comment(lib, "netapi32.lib")

BOOL AddMachineAccount(
    LPWSTR wTargetComputer,
    LPWSTR MachineAccount,
    DWORD AccountType
    )
{
    LPWSTR wAccount;
    LPWSTR wPassword;
    USER_INFO_1 ui;
    DWORD cbAccount;
    DWORD cbLength;
    DWORD dwError;

    //
    // Ensure a valid computer account type was passed.
    //
    if (AccountType != UF_WORKSTATION_TRUST_ACCOUNT &&
        AccountType != UF_SERVER_TRUST_ACCOUNT &&
        AccountType != UF_INTERDOMAIN_TRUST_ACCOUNT
        ) 
    {
        SetLastError(ERROR_INVALID_PARAMETER);
        return FALSE;
    }

    //
    // Obtain number of chars in computer account name.
    //
    cbLength = cbAccount = lstrlenW(MachineAccount);

    //
    // Ensure computer name doesn't exceed maximum length.
    //
    if(cbLength > MAX_COMPUTERNAME_LENGTH) {
        SetLastError(ERROR_INVALID_ACCOUNT_NAME);
        return FALSE;
    }

    //
    // Allocate storage to contain Unicode representation of
    // computer account name + trailing $ + NULL.
    //
    wAccount=(LPWSTR)HeapAlloc(GetProcessHeap(), 0,
        (cbAccount + 1 + 1) * sizeof(WCHAR)  // Account + '$' + NULL
        );

    if(wAccount == NULL) return FALSE;

    //
    // Password is the computer account name converted to lowercase;
    //  you will convert the passed MachineAccount in place.
    //
    wPassword = MachineAccount;

    //
    // Copy MachineAccount to the wAccount buffer allocated while
    //  converting computer account name to uppercase.
    //  Convert password (in place) to lowercase.
    //
    while(cbAccount--) {
        wAccount[cbAccount] = towupper( MachineAccount[cbAccount] );
        wPassword[cbAccount] = towlower( wPassword[cbAccount] );
    }

    //
    // Computer account names have a trailing Unicode '$'.
    //
    wAccount[cbLength] = L'$';
    wAccount[cbLength + 1] = L'\0'; // terminate the string

    //
    // If the password is greater than the max allowed, truncate.
    //
    if(cbLength > LM20_PWLEN) wPassword[LM20_PWLEN] = L'\0';

    //
    // Initialize the USER_INFO_1 structure.
    //
    ZeroMemory(&ui, sizeof(ui));

    ui.usri1_name = wAccount;
    ui.usri1_password = wPassword;

    ui.usri1_flags = AccountType | UF_SCRIPT;
    ui.usri1_priv = USER_PRIV_USER;

    dwError=NetUserAdd(
                wTargetComputer,    // target computer name
                1,                  // info level
                (LPBYTE) &ui,       // buffer
                NULL
                );

    //
    // Free allocated memory.
    //
    if(wAccount) HeapFree(GetProcessHeap(), 0, wAccount);

    //
    // Indicate whether the function was successful.
    //
    if(dwError == NO_ERROR)
        return TRUE;
    else {
        SetLastError(dwError);
        return FALSE;
    }
}
```



<span data-ttu-id="2d2ab-118">O usuário que chama as funções de gerenciamento de conta deve ter privilégios de administrador no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-118">The user that calls the account management functions must have Administrator privilege on the target computer.</span></span> <span data-ttu-id="2d2ab-119">No caso de contas de computador existentes, o criador da conta pode gerenciar a conta, independentemente da Associação administrativa.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-119">In the case of existing computer accounts, the creator of the account can manage the account, regardless of administrative membership.</span></span> <span data-ttu-id="2d2ab-120">Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="2d2ab-120">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="2d2ab-121">O SeMachineAccountPrivilege pode ser concedido no computador de destino para fornecer aos usuários especificados a capacidade de criar contas de computador.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-121">The SeMachineAccountPrivilege can be granted on the target computer to give specified users the ability to create computer accounts.</span></span> <span data-ttu-id="2d2ab-122">Isso dá aos não administradores a capacidade de criar contas de computador.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-122">This gives non-administrators the ability to create computer accounts.</span></span> <span data-ttu-id="2d2ab-123">O chamador precisa habilitar esse privilégio antes de adicionar a conta de computador.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-123">The caller needs to enable this privilege prior to adding the computer account.</span></span> <span data-ttu-id="2d2ab-124">Para obter mais informações sobre privilégios de conta, consulte [constantes](/windows/desktop/SecAuthZ/authorization-constants)de [privilégios](/windows/desktop/SecAuthZ/privileges) e autorização.</span><span class="sxs-lookup"><span data-stu-id="2d2ab-124">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

 

 