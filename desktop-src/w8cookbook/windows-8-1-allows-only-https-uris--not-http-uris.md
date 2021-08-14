---
title: URIs em Windows 8.1
description: Windows 8.1 permite apenas uris https, não URIs http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3246cad0fb6114a3a01d781ed990e0c277547e2b9ee489572c8124a23e7e81b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028804"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 permite apenas uris https, não URIs http

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
servidores-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

embora os aplicativos criados para Windows 8 possam incluir uris http e https em seus uris de conteúdo de aplicativo, os aplicativos criados para Windows 8.1 podem incluir somente URIs https.

A única exceção é para ContentUriRules dinâmicos que são especificados no arquivo de AppxManifest.xml do aplicativo. Com o Dynamic ContentUriRules, os aplicativos podem acessar domínios ou recursos de rede adicionais que são fornecidos pelo administrador, como URIs de Política de Grupo. no entanto, os ContentUriRules dinâmicos só estarão disponíveis para Windows aplicativos da loja se atenderem a essas condições:

-   O Política de Grupo está habilitado
-   O pacote especificou o recurso enterpriseAuthentication
-   o OSMaxVersionTested do pacote é Windows 8.1 ou superior

as novas restrições no Windows 8.1 fazem parte das restrições de segurança aprimoradas para proteger ainda mais a plataforma.

## <a name="manifestations"></a>Manifestações

ao executar um aplicativo criado para Windows 8 no Windows 8.1, o uso de URIs http no [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) é permitido.

## <a name="mitigations"></a>Atenuações

Recomendamos que os desenvolvedores de WWA mudem de [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) para o controle [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-MS-WebView>). No entanto, se você precisar de suporte para AppCache, IndexedDB, geolocalização ou acesso de área de transferência programático, será necessário continuar usando o <iframe> para Windows 8.1.

Uso contínuo de <iframe> para o conteúdo remoto, será necessário uma nova entrada no ApplicationContentUriRules para o aplicativo. Os aplicativos com WebView exigem novas entradas no ApplicationContentUriRules se o conteúdo da Web precisar invocar Window. external. Notify para gerar um evento [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) . se você não tiver Visual Studio, poderá atualizar o manifesto do aplicativo adicionando o seguinte XML, incluindo curingas para subdomínios (por exemplo, https:// \* . microsoft.com):


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a>Recursos

-   [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<iframe>objeto de elemento \| <iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [Classe WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [Evento WebView. ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 