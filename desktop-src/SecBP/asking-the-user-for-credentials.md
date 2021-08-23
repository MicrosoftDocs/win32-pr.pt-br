---
description: Seu aplicativo pode precisar solicitar ao usuário informações de nome de usuário e senha para evitar o armazenamento de uma senha de administrador ou verificar se o token contém os privilégios apropriados.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Solicitando credenciais ao usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9b9941be168a307e35b3575f4d12241dc624553686a61b232f2c5ba86e9c0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480486"
---
# <a name="asking-the-user-for-credentials"></a>Solicitando credenciais ao usuário

Seu aplicativo pode precisar solicitar ao usuário informações de nome de usuário e senha para evitar o armazenamento de uma senha de administrador ou verificar se o token contém os privilégios apropriados.

No entanto, simplesmente solicitar credenciais pode treinar os usuários a fornená-los a qualquer caixa de diálogo aleatória e não identificada exibida na tela. O procedimento a seguir é recomendado para reduzir esse efeito de treinamento.

**Para adquirir corretamente as credenciais do usuário**

1.  Informe ao usuário, usando uma mensagem que faz claramente parte do seu aplicativo, que ele verá uma caixa de diálogo que solicita seu nome de usuário e senha. Você também pode usar a estrutura [**CREDUI \_ INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) na chamada para [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para transmitir dados de identificação ou uma mensagem.
2.  Chame [**CredUIPromptForCredentials.**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) Observe que o número máximo de caracteres especificado para informações de nome de usuário e senha inclui o caractere nulo de terminação.
3.  Chame [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) e [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) para verificar se você obteve as credenciais apropriadas.

O exemplo a seguir mostra como chamar [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para solicitar ao usuário um nome de usuário e uma senha. Ele começa preenchendo uma estrutura CREDUI \_ INFO com informações sobre quais prompts usar. Em seguida, o código preenche dois buffers com zeros. Isso é feito para garantir que nenhuma informação seja passada para a função que possa revelar um nome de usuário antigo ou uma senha para o usuário. A chamada para **CredUIPromptForCredentials** abrirá a caixa de diálogo. Por motivos de segurança, este exemplo usa o sinalizador SINALIZADORES CREDUI NÃO PERSISTir para impedir que o sistema operacional armazenar a senha porque ela pode \_ \_ ser \_ \_ exposta. Se não houver erros, **CredUIPromptForCredentials** preencherá as variáveis pszName e pszPwd e retornará zero. Quando o aplicativo terminar de usar as credenciais, ele deverá colocar zeros nos buffers para impedir que as informações seja acidentalmente reveladas.


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

 

 
