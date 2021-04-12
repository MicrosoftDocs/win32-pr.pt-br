---
title: URIs em Windows 8.1
description: Windows 8.1 permite apenas URIs HTTPS, não URIs http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366554"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 permite apenas URIs HTTPS, não URIs http

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Servidores-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

Embora os aplicativos criados para o Windows 8 possam incluir URIs http e HTTPS em seus URIs de conteúdo de aplicativo, os aplicativos criados para Windows 8.1 podem incluir somente URIs HTTPS.

A única exceção é para ContentUriRules dinâmicos que são especificados no arquivo de AppxManifest.xml do aplicativo. Com o Dynamic ContentUriRules, os aplicativos podem acessar domínios ou recursos de rede adicionais que são fornecidos pelo administrador, como URIs de Política de Grupo. No entanto, os ContentUriRules dinâmicos só estarão disponíveis para aplicativos da Windows Store se atenderem a estas condições:

-   O Política de Grupo está habilitado
-   O pacote especificou o recurso enterpriseAuthentication
-   O OSMaxVersionTested do pacote é Windows 8.1 ou superior

As novas restrições no Windows 8.1 fazem parte das restrições de segurança aprimoradas para proteger ainda mais a plataforma.

## <a name="manifestations"></a>Manifestações

Ao executar um aplicativo criado para o Windows 8 em Windows 8.1, o uso de URIs http no [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) é permitido.

## <a name="mitigations"></a>Atenuações

Recomendamos que os desenvolvedores de WWA mudem de [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) para o controle [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-MS-WebView>). No entanto, se você precisar de suporte para AppCache, IndexedDB, geolocalização ou acesso de área de transferência programático, será necessário continuar usando o <iframe> para Windows 8.1.

Uso contínuo de <iframe> para o conteúdo remoto, será necessário uma nova entrada no ApplicationContentUriRules para o aplicativo. Os aplicativos com WebView exigem novas entradas no ApplicationContentUriRules se o conteúdo da Web precisar invocar Window. external. Notify para gerar um evento [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) . Se você não tiver o Visual Studio, poderá atualizar o manifesto do aplicativo adicionando o seguinte XML, incluindo curingas para subdomínios (por exemplo, https:// \* . Microsoft.com):


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

 

 