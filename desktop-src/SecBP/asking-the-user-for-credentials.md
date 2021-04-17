---
description: Seu aplicativo pode precisar solicitar ao usuário informações de nome de usuário e senha para evitar o armazenamento de uma senha de administrador ou para verificar se o token contém os privilégios apropriados.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Solicitando credenciais ao usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adb315837d86a9f1dda4075b8d89db33f0dd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770259"
---
# <a name="asking-the-user-for-credentials"></a><span data-ttu-id="d75ce-103">Solicitando credenciais ao usuário</span><span class="sxs-lookup"><span data-stu-id="d75ce-103">Asking the User for Credentials</span></span>

<span data-ttu-id="d75ce-104">Seu aplicativo pode precisar solicitar ao usuário informações de nome de usuário e senha para evitar o armazenamento de uma senha de administrador ou para verificar se o token contém os privilégios apropriados.</span><span class="sxs-lookup"><span data-stu-id="d75ce-104">Your application may need to prompt the user for user name and password information to avoid storing an administrator password or to verify that the token holds the appropriate privileges.</span></span>

<span data-ttu-id="d75ce-105">No entanto, a simples solicitação de credenciais pode treinar os usuários a fornecê-los a qualquer caixa de diálogo aleatória e não identificada que aparece na tela.</span><span class="sxs-lookup"><span data-stu-id="d75ce-105">However, simply prompting for credentials may train users to supply those to any random, unidentified dialog box that appears on the screen.</span></span> <span data-ttu-id="d75ce-106">O procedimento a seguir é recomendado para reduzir esse efeito de treinamento.</span><span class="sxs-lookup"><span data-stu-id="d75ce-106">The following procedure is recommended to reduce that training effect.</span></span>

<span data-ttu-id="d75ce-107">**Para adquirir credenciais de usuário corretamente**</span><span class="sxs-lookup"><span data-stu-id="d75ce-107">**To properly acquire user credentials**</span></span>

1.  <span data-ttu-id="d75ce-108">Informe o usuário, usando uma mensagem que é claramente parte do seu aplicativo, que verá uma caixa de diálogo que solicita seu nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="d75ce-108">Inform the user, by using a message that is clearly part of your application, that they will see a dialog box that requests their user name and password.</span></span> <span data-ttu-id="d75ce-109">Você também pode usar a estrutura de [**\_ informações CREDUI**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) na chamada para [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para transmitir dados de identificação ou uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d75ce-109">You can also use the [**CREDUI\_INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) structure on the call to [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to convey identifying data or a message.</span></span>
2.  <span data-ttu-id="d75ce-110">Chame [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="d75ce-110">Call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span></span> <span data-ttu-id="d75ce-111">Observe que o número máximo de caracteres especificado para informações de nome de usuário e senha inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="d75ce-111">Note that the maximum number of characters specified for user name and password information includes the terminating null character.</span></span>
3.  <span data-ttu-id="d75ce-112">Chame [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) e [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) para verificar se você obteve as credenciais apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d75ce-112">Call [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) and [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) to verify that you obtained appropriate credentials.</span></span>

<span data-ttu-id="d75ce-113">O exemplo a seguir mostra como chamar [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para solicitar ao usuário um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="d75ce-113">The following example shows how to call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to ask the user for a user name and password.</span></span> <span data-ttu-id="d75ce-114">Ele começa preenchendo uma estrutura de informações de CREDUI \_ com informações sobre quais prompts usar.</span><span class="sxs-lookup"><span data-stu-id="d75ce-114">It begins by filling in a CREDUI\_INFO structure with information about what prompts to use.</span></span> <span data-ttu-id="d75ce-115">Em seguida, o código preenche dois buffers com zeros.</span><span class="sxs-lookup"><span data-stu-id="d75ce-115">Next, the code fills two buffers with zeros.</span></span> <span data-ttu-id="d75ce-116">Isso é feito para garantir que nenhuma informação seja passada para a função que possa revelar um nome de usuário ou senha antigo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="d75ce-116">This is done to ensure that no information gets passed to the function that might reveal an old user name or password to the user.</span></span> <span data-ttu-id="d75ce-117">A chamada para **CredUIPromptForCredentials** abre a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d75ce-117">The call to **CredUIPromptForCredentials** brings up the dialog box.</span></span> <span data-ttu-id="d75ce-118">Por motivos de segurança, este exemplo usa o \_ sinalizador CREDUI flags \_ \_ não \_ persiste para impedir que o sistema operacional armazene a senha, pois ela pode ser exposta.</span><span class="sxs-lookup"><span data-stu-id="d75ce-118">For security reasons, this example uses the CREDUI\_FLAGS\_DO\_NOT\_PERSIST flag to prevent the operating system from storing the password because it might then be exposed.</span></span> <span data-ttu-id="d75ce-119">Se não houver erros, **CredUIPromptForCredentials** preencherá as variáveis PszName e pszPwd e retornará zero.</span><span class="sxs-lookup"><span data-stu-id="d75ce-119">If there are no errors, **CredUIPromptForCredentials** fills in the pszName and pszPwd variables and returns zero.</span></span> <span data-ttu-id="d75ce-120">Quando o aplicativo termina de usar as credenciais, ele deve colocar zeros nos buffers para impedir que as informações sejam reveladas acidentalmente.</span><span class="sxs-lookup"><span data-stu-id="d75ce-120">When the application has finished using the credentials, it should put zeros in the buffers to prevent the information from being accidentally revealed.</span></span>


```C++
CREDUI_INFO cui;
TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH+1];
TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1];
BOOL fSave;
DWORD dwErr;
 
cui.cbSize = sizeof(CREDUI_INFO);
cui.hwndParent = NULL;
//  Ensure that MessageText and CaptionText identify what credentials
//  to use and which application requires them.
cui.pszMessageText = TEXT("Enter administrator account information");
cui.pszCaptionText = TEXT("CredUITest");
cui.hbmBanner = NULL;
fSave = FALSE;
SecureZeroMemory(pszName, sizeof(pszName));
SecureZeroMemory(pszPwd, sizeof(pszPwd));
dwErr = CredUIPromptForCredentials( 
    &cui,                         // CREDUI_INFO structure
    TEXT("TheServer"),            // Target for credentials
                                  //   (usually a server)
    NULL,                         // Reserved
    0,                            // Reason
    pszName,                      // User name
    CREDUI_MAX_USERNAME_LENGTH+1, // Max number of char for user name
    pszPwd,                       // Password
    CREDUI_MAX_PASSWORD_LENGTH+1, // Max number of char for password
    &fSave,                       // State of save check box
    CREDUI_FLAGS_GENERIC_CREDENTIALS |  // flags
    CREDUI_FLAGS_ALWAYS_SHOW_UI |
    CREDUI_FLAGS_DO_NOT_PERSIST);  

if(!dwErr)
{
    //  Put code that uses the credentials here.
 
    //  When you have finished using the credentials,
    //  erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
}
```



## <a name="related-topics"></a><span data-ttu-id="d75ce-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d75ce-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d75ce-122">**CredUICmdLinePromptForCredentials**</span><span class="sxs-lookup"><span data-stu-id="d75ce-122">**CredUICmdLinePromptForCredentials**</span></span>](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[<span data-ttu-id="d75ce-123">**CREDUI \_ UINFO**</span><span class="sxs-lookup"><span data-stu-id="d75ce-123">**CREDUI\_UINFO**</span></span>](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
