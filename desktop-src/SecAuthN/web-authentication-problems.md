---
description: Este tópico descreve as dicas de solução de problemas para usar as APIs do agente de autenticação da Web para suas páginas da Web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problemas de autenticação da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c722aefa35849485d2c8958e17c654b5bb6477479ac1765e76e648fe15f9826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785856"
---
# <a name="web-authentication-problems"></a>Problemas de autenticação da Web

Este tópico descreve as dicas de solução de problemas para usar as APIs do agente de autenticação da Web para suas páginas da Web.

-   [Logs operacionais](#operational-logs)
-   [Usando o Fiddler com o agente de autenticação da Web](#using-fiddler-with-web-authentication-broker)
-   [Tópicos relacionados](#related-topics)

## <a name="operational-logs"></a>Logs operacionais

Geralmente é possível determinar o que não está funcionando usando logs operacionais. há um canal de log de eventos dedicado Microsoft-Windows-webauth \\ operacional que permite aos desenvolvedores de sites entender como suas páginas da web estão sendo processadas pelo agente de autenticação da web. para habilitá-lo, inicie eventvwr.exe e habilite o log operacional no aplicativo e serviços \\ Microsoft \\ Windows \\ webauth. Além disso, o agente de autenticação da Web acrescenta uma cadeia de caracteres exclusiva à cadeia de caracteres do agente do usuário para se identificar no servidor Web. A cadeia de caracteres é "MSAuthHost/1.0". Observe que o número da versão pode mudar no futuro, portanto você não deve depender do número daquela versão no seu código. Um exemplo da cadeia de caracteres do agente de usuário completo é o seguinte:

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

Exemplo de uso de logs operacionais

1.  Habilitar logs operacionais
2.  Executar o aplicativo social da contoso![visualizador de Eventos exibindo logs operacionais do webauth](images/wab-figure15.png)
3.  As entradas de logs geradas podem ser usadas para entender o comportamento do agente de autenticação da Web com mais detalhes. Nesse caso, elas podem ser:
    -   Início da Navegação: registra quando o AuthHost é iniciado e contém informações sobre as URLs de início e término.
    -   ![ilustra os detalhes do início da navegação](images/wab-figure16.png)
    -   Navegação Completa: registra a conclusão do carregamento de uma página da Web.
    -   Marca meta: registra quando uma marca meta é encontrada, incluindo os detalhes.
    -   Término da Navegação: navegação encerrada pelo usuário.
    -   Erro de Navegação: o AuthHost encontra um erro de navegação em uma URL, incluindo HttpStatusCode.
    -   Final da Navegação: a URL de término é encontrada.

## <a name="using-fiddler-with-web-authentication-broker"></a>Usando o Fiddler com o agente de autenticação da Web

o depurador da web do Fiddler pode ser usado com Windows 8 aplicativos.

1.  Por o AuthHost executar no seu próprio contêiner de aplicativo para dar maior capacidade de rede privada, você deve definir uma chave de registro: Windows Registry Editor Version 5.00

    **HKEY \_ \_** \\ opções de execução de arquivo de imagem do **SOFTWARE** do computador LOCAL \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\  \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001<dl> <dt>

                     Data type
</dt> <dd>                     DWORD</dd> </dl>

2.  Adicione uma regra para o AuthHost, uma vez que é ele quem gera o tráfego de saída.
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  Adicione uma regra de firewall para o tráfego de entrada ao Fiddler.

para obter mais informações, consulte o [Blog sobre como usar o depurador da web do Fiddler com aplicativos da Windows Store](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações para o desenvolvimento de páginas da Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Perguntas frequentes sobre o agente de autenticação da Web](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041&preserve-view=true)
</dt> </dl>

 

 
