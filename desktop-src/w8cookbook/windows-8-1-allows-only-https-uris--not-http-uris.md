---
title: URIs em Windows 8.1
description: Windows 8.1 permite apenas URIs https, não URIs http
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
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 permite apenas URIs https, não URIs http

## <a name="platforms"></a>Plataformas

<dl> Clientes – Windows 8.1  
Servidores – Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

Embora os aplicativos Windows 8 possam incluir URIs http e https em seus URIs de conteúdo do aplicativo, os aplicativos Windows 8.1 podem incluir apenas URIs https.

A única exceção é para ContentUriRules dinâmico especificado no arquivo AppxManifest.xml aplicativo. Com o ContentUriRules dinâmico, os aplicativos podem acessar domínios adicionais ou recursos de rede fornecidos pelo administrador, como uris Política de Grupo dados. No entanto, ContentUriRules dinâmico só estará disponível para aplicativos Windows Store se atenderem a estas condições:

-   A Política de Grupo está habilitada
-   O pacote especificou a funcionalidade enterpriseAuthentication
-   OSMaxVersionTested do pacote é Windows 8.1 ou superior

As novas restrições no Windows 8.1 fazem parte das restrições de segurança aprimoradas para proteger ainda mais a plataforma.

## <a name="manifestations"></a>Manifestações

Ao executar um aplicativo criado para Windows 8 no Windows 8.1, o uso de URIs http no [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) é permitido.

## <a name="mitigations"></a>Atenuações

Recomendamos que os desenvolvedores do WWA alternem de para o controle [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-webview>). No entanto, se você precisar de suporte para AppCache, IndexedDB, localização geográfica ou acesso de área de transferência programática, você precisará continuar usando <iframe> para Windows 8.1.

Uso contínuo de <iframe> para conteúdo remoto exigirá uma nova entrada no ApplicationContentUriRules para o aplicativo. Os aplicativos com WebView exigirão novas entradas no ApplicationContentUriRules se o conteúdo da Web precisar invocar window.external.notify para gerar um [evento ScriptNotify.](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) Se você não tiver Visual Studio, poderá atualizar o manifesto do aplicativo adicionando o seguinte XML, incluindo curingas para subdomasins (por exemplo, https:// \* .microsoft.com):


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
-   [<iframe> objeto \| <iframe> element](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [Classe Webview](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [Evento WebView.ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 