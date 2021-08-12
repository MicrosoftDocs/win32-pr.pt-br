---
title: Temas Alto Contraste suporte
description: Este tópico compara o suporte para temas de alto contraste no Windows 8 com o das versões anteriores do Windows e explica como dar suporte a temas de alto contraste em um Windows 8 aplicativo.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f32c89302daeb7190174a0d6b9e822e1c55d3e530ad29baedd00c5ffdefc97b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670610"
---
# <a name="supporting-high-contrast-themes"></a>Temas Alto Contraste suporte

Este tópico compara o suporte para temas de alto contraste no Windows 8 com o das versões anteriores do Windows e explica como dar suporte a temas de alto contraste em um Windows 8 aplicativo.

Ele inclui as seções a seguir.

-   [Visão geral do suporte para Alto Contraste temas](#overview-of-support-for-high-contrast-themes)
-   [Suporte Alto Contraste temas em Windows 8 e posteriores](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Adicionando uma seção de compatibilidade ao manifesto do aplicativo](#adding-a-compatibility-section-to-your-application-manifest)
-   [Detectando Alto Contraste em versões anteriores do Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Visão geral do suporte para Alto Contraste temas

Windows 7 e anteriores são suportados por dois modelos de temas, incluindo o modelo Windows clássico herdado e os estilos visuais atuais. O Windows modelo clássico foi mantido por meio Windows 7 principalmente para dar suporte aos vários temas de alto contraste. No entanto, Windows modelo clássico tem várias desvantagens:

-   Não há suporte para temas que usam estilos visuais, como Windows Aero. Os usuários de temas de alto contraste devem usar a Windows interface do usuário clássica.
-   Não há suporte para recursos de interface do usuário que dependem da Gerenciador de Janelas da Área de Trabalho (DWM) para executar, como visualizações em miniatura e a lupa de tela inteira que foi introduzida no Windows 7.
-   Os desenvolvedores devem manter dois caminhos de código separados para dar suporte aos dois modelos de temas diferentes.

No Windows 8 e posterior, as seguintes alterações no modelo de temas abordam as desvantagens anteriores:

-   O Windows modelo de temas clássico não tem mais suporte, permitindo que os desenvolvedores mantenham apenas um caminho de código para aplicativos destinados apenas a Windows 8.
-   Como os estilos visuais e o DWM estão em Windows 8, os usuários de alto contraste têm acesso a recursos como visualizações em miniatura e a lupa de tela inteira.
-   Os estilos visuais dão suporte à definição das cores de vários elementos da interface do usuário, permitindo que os usuários de alto contraste personalizem a interface do usuário para acomodar preferências e necessidades individuais.
-   Windows 8 inclui suporte à compatibilidade para aplicativos existentes que foram projetados para usar temas de alto contraste com base no Windows de temas clássico.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>Suporte Alto Contraste temas em Windows 8 e posteriores

No Windows 8, como os estilos visuais estão em modo de alto contraste, dar suporte a temas de alto contraste é simples, desde que você tenha seguido as diretrizes a seguir.

-   Tamanhos de fonte e controle. Para garantir que sua interface do usuário seja acessível a usuários com deficiências, depure os tamanhos de fonte de acordo com as configurações de tema atuais. De definir o tamanho dos controles como pelo menos o tamanho padrão.
-   Cores. Evite usar cores em código. Em vez disso, use as cores do sistema porque elas se baseiam no tema atual. O uso de cores personalizadas pode interferir e substituir as cores nos temas de alto contraste.
-   Manifesto do aplicativo. Os aplicativos projetados para trabalhar com os novos temas de alto contraste devem ter uma seção de compatibilidade de aplicativo definida em seu manifesto que contém os GUIDs de Windows 8 compatibilidade. Caso contrário, Windows assume que o aplicativo foi projetado para uma versão mais antiga do Windows e renderiza a interface do usuário do aplicativo simulando o Windows de temas clássico.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Adicionando uma seção de compatibilidade ao manifesto do aplicativo

Um manifesto do aplicativo é um arquivo XML que descreve os requisitos de um aplicativo. A seção de compatibilidade do manifesto identifica as versões Windows com suporte pelo aplicativo. Os GUIDs a seguir são usados na seção de compatibilidade para identificar as várias versões do Windows.

| Versão       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

A seção de compatibilidade pode especificar várias versões Windows, mas cada uma deve estar contida em sua própria `<supportedOS/>` marca. O exemplo a seguir mostra um manifesto do aplicativo que especifica Windows 7 e Windows 8 na seção de compatibilidade:


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



Se um aplicativo não tiver um manifesto de compatibilidade, supõe-se que ele seja um aplicativo Windows Vista e não use controles temáticos na área do cliente quando um tema de alto contraste estiver ativo. Além disso, o comportamento de algumas funções de estilos visuais é afetado. Por exemplo, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)e [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) retornam FALSE, enquanto [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) e [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) retornam um handle NULL. Isso é para suporte de compatibilidade, de modo que os aplicativos construídos antes do Windows 8 ainda possam renderizar sua interface do usuário na mesma aparência que o modo de alto contraste das versões anteriores do Windows em que os estilos visuais não estão disponíveis.

No Windows 8, o aplicativo ainda recebe os benefícios da composição da área de trabalho. Isso significa, por exemplo, que os aplicativos de usabilidade, como a lupa de tela inteira, não dependem do status do manifesto de um aplicativo individual. O aplicativo de usabilidade continua a funcionar no modo de alto contraste com um aplicativo que não se identifica como Windows 8 compatível em seu manifesto.

As imagens a seguir mostram uma caixa de diálogo simples em alto contraste Windows 7.

![caixa de diálogo de contraste de hig](images/win7-high-contrast.png)

Essa imagem mostra a mesma caixa de diálogo em alto contraste no Windows 8, mas com Windows 7 especificada no manifesto do aplicativo:

![caixa de diálogo de alto contraste w8](images/win7-compat.png)

Essa imagem mostra a mesma caixa de diálogo em alto contraste Windows 8, com Windows 8 especificado no manifesto do aplicativo:

![caixa de diálogo de alto contraste w8 com manifesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Detectando Alto Contraste em versões anteriores do Windows

Aplicativos em execução em versões anteriores Windows não têm acesso aos novos temas de alto contraste. Se o aplicativo precisar ser executado em versões anteriores do , você deverá incluir suporte para renderizar sua interface do usuário em alto contraWindowsst no modelo de temas Windows clássico. Seu aplicativo pode determinar se um tema de alto contraste está ativo chamando a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o **sinalizador SPI \_ GETHIGHCONTRAST.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitar estilos visuais](cookbook-overview.md)
</dt> <dt>

[Estilos visuais](themes-overview.md)
</dt> </dl>

 

 