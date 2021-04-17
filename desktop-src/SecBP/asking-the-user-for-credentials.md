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
# <a name="asking-the-user-for-credentials"></a>Solicitando credenciais ao usuário

Seu aplicativo pode precisar solicitar ao usuário informações de nome de usuário e senha para evitar o armazenamento de uma senha de administrador ou para verificar se o token contém os privilégios apropriados.

No entanto, a simples solicitação de credenciais pode treinar os usuários a fornecê-los a qualquer caixa de diálogo aleatória e não identificada que aparece na tela. O procedimento a seguir é recomendado para reduzir esse efeito de treinamento.

**Para adquirir credenciais de usuário corretamente**

1.  Informe o usuário, usando uma mensagem que é claramente parte do seu aplicativo, que verá uma caixa de diálogo que solicita seu nome de usuário e senha. Você também pode usar a estrutura de [**\_ informações CREDUI**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) na chamada para [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para transmitir dados de identificação ou uma mensagem.
2.  Chame [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa). Observe que o número máximo de caracteres especificado para informações de nome de usuário e senha inclui o caractere nulo de terminação.
3.  Chame [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) e [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) para verificar se você obteve as credenciais apropriadas.

O exemplo a seguir mostra como chamar [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para solicitar ao usuário um nome de usuário e uma senha. Ele começa preenchendo uma estrutura de informações de CREDUI \_ com informações sobre quais prompts usar. Em seguida, o código preenche dois buffers com zeros. Isso é feito para garantir que nenhuma informação seja passada para a função que possa revelar um nome de usuário ou senha antigo para o usuário. A chamada para **CredUIPromptForCredentials** abre a caixa de diálogo. Por motivos de segurança, este exemplo usa o \_ sinalizador CREDUI flags \_ \_ não \_ persiste para impedir que o sistema operacional armazene a senha, pois ela pode ser exposta. Se não houver erros, **CredUIPromptForCredentials** preencherá as variáveis PszName e pszPwd e retornará zero. Quando o aplicativo termina de usar as credenciais, ele deve colocar zeros nos buffers para impedir que as informações sejam reveladas acidentalmente.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[**CREDUI \_ UINFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
