---
title: Suporte a temas de Alto Contraste
description: Este tópico compara o suporte para temas de alto contraste no Windows 8 para as versões anteriores do Windows e explica como dar suporte a temas de alto contraste em um aplicativo do Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824002"
---
# <a name="supporting-high-contrast-themes"></a>Suporte a temas de Alto Contraste

Este tópico compara o suporte para temas de alto contraste no Windows 8 para as versões anteriores do Windows e explica como dar suporte a temas de alto contraste em um aplicativo do Windows 8.

Ele inclui as seções a seguir.

-   [Visão geral do suporte para temas de Alto Contraste](#overview-of-support-for-high-contrast-themes)
-   [Suporte a temas de Alto Contraste no Windows 8 e posterior](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Adicionando uma seção de compatibilidade ao manifesto do aplicativo](#adding-a-compatibility-section-to-your-application-manifest)
-   [Detectando Alto Contraste em versões anteriores do Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Visão geral do suporte para temas de Alto Contraste

O Windows 7 e versões anteriores dão suporte a dois modelos de temas, incluindo o modelo clássico do Windows herdado e os estilos visuais atuais. O modelo clássico do Windows foi mantido pelo Windows 7 principalmente para dar suporte a vários temas de alto contraste. No entanto, o modelo clássico do Windows tem uma série de desvantagens:

-   Não há suporte para temas que usam estilos visuais, como o Windows Aero. Os usuários de temas de alto contraste devem usar a interface do usuário clássica do Windows.
-   Não há suporte para recursos de interface do usuário que dependem de Gerenciador de Janelas da Área de Trabalho (DWM) para execução, como visualizações de miniatura e a lupa de tela cheia que foi introduzida no Windows 7.
-   Os desenvolvedores devem manter dois caminhos de código separados para dar suporte aos dois modelos de temas diferentes.

No Windows 8 e posterior, as seguintes alterações no modelo de temas abordam as desvantagens anteriores:

-   O modelo de tema clássico do Windows não tem mais suporte, permitindo que os desenvolvedores mantenham apenas um caminho de código para aplicativos direcionados apenas para o Windows 8.
-   Como os estilos visuais e o DWM estão no Windows 8, os usuários de alto contraste têm acesso a recursos como visualizações de miniatura e a lupa de tela inteira.
-   Os estilos visuais dão suporte à definição das cores de vários elementos da interface do usuário, permitindo que usuários de alto contraste personalizem a interface do usuário para acomodar necessidades e preferências individuais.
-   O Windows 8 inclui suporte de compatibilidade para aplicativos existentes que são projetados para usar temas de alto contraste com base no modelo clássico do Windows.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>Suporte a temas de Alto Contraste no Windows 8 e posterior

No Windows 8, como os estilos visuais estão no modo de alto contraste, o suporte a temas de alto contraste é muito simples, desde que você preste atenção às diretrizes a seguir.

-   Tamanhos de fonte e de controle. Para garantir que sua interface do usuário seja acessível a usuários com deficiências, defina tamanhos de fonte de acordo com as configurações de tema atuais. Defina o tamanho dos controles como, pelo menos, o tamanho padrão.
-   Cores. Evite usar cores embutidas em código. Em vez disso, use as cores do sistema porque elas se baseiam no tema atual. O uso de cores personalizadas pode interferir e substituir as cores nos temas de alto contraste.
-   Manifesto do aplicativo. Os aplicativos projetados para trabalhar com os novos temas de alto contraste devem ter uma seção de compatibilidade de aplicativos definida em seu manifesto que contenha os GUIDs de compatibilidade do Windows 8. Caso contrário, o Windows pressupõe que o aplicativo foi projetado para uma versão mais antiga do Windows e renderiza a interface do usuário do aplicativo simulando o modelo clássico de tema do Windows.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Adicionando uma seção de compatibilidade ao manifesto do aplicativo

Um manifesto de aplicativo é um arquivo XML que descreve os requisitos de um aplicativo. A seção de compatibilidade do manifesto identifica as versões do Windows com suporte no aplicativo. Os GUIDs a seguir são usados na seção de compatibilidade para identificar as várias versões do Windows.

| Versão       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

A seção de compatibilidade pode especificar várias versões do Windows, mas cada uma delas deve estar contida em sua própria `<supportedOS/>` marca. O exemplo a seguir mostra um manifesto do aplicativo que especifica o Windows 7 e o Windows 8 na seção de compatibilidade:


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



Se um aplicativo não tiver um manifesto de compatibilidade, ele será considerado um aplicativo do Windows Vista e não usará controles com temas na área do cliente quando um tema de alto contraste estiver ativo. Além disso, o comportamento de algumas funções de estilos visuais é afetado. Por exemplo, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)e [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) retornam false, enquanto [**OPENTHEMEDATA**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) e [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) retornam um identificador nulo. Isso é para o suporte à compatibilidade, de modo que os aplicativos criados antes do Windows 8 ainda possam renderizar sua interface do usuário da mesma forma que o modo de alto contraste das versões anteriores do Windows em que os estilos visuais não estão disponíveis.

No Windows 8, o aplicativo ainda recebe os benefícios da composição da área de trabalho. Isso significa, por exemplo, que aplicativos de usabilidade, como a lupa de tela inteira, não dependem do status de um manifesto de aplicativo individual. O aplicativo de usabilidade continua funcionando no modo de alto contraste com um aplicativo que não se identifica como compatível com o Windows 8 em seu manifesto.

As imagens a seguir mostram uma caixa de diálogo simples em alto contraste no Windows 7.

![caixa de diálogo hig Contrast](images/win7-high-contrast.png)

Essa imagem mostra a mesma caixa de diálogo em alto contraste no Windows 8, mas com a compatibilidade com o Windows 7 especificada no manifesto do aplicativo:

![W8 caixa de diálogo de alto contraste](images/win7-compat.png)

Essa imagem mostra a mesma caixa de diálogo em alto contraste no Windows 8, com o Windows 8 especificado no manifesto do aplicativo:

![caixa de diálogo de alto contraste do W8 com manifesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Detectando Alto Contraste em versões anteriores do Windows

Os aplicativos executados em versões anteriores do Windows não têm acesso aos novos temas de alto contraste. Se seu aplicativo precisar ser executado em versões anteriores do, você deverá incluir o suporte para renderizar sua interface do usuário em alta contraWindowsst no modelo clássico de tema do Windows. Seu aplicativo pode determinar se um tema de alto contraste está ativo chamando a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o sinalizador **SPI \_ GETHIGHCONTRAST** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitar estilos visuais](cookbook-overview.md)
</dt> <dt>

[Estilos visuais](themes-overview.md)
</dt> </dl>

 

 