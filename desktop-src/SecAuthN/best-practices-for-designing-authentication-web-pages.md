---
description: Este tópico descreve as práticas recomendadas para a criação de páginas da Web que usam o agente de autenticação da Web para fazer logon.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Melhores práticas para o design de páginas da Web de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdd6ab5dc067c23cfb29d21d2ff4780cee0ef1c
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353669"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Melhores práticas para o design de páginas da Web de autenticação

Este tópico descreve as práticas recomendadas para a criação de páginas da Web que usam o agente de autenticação da Web para fazer logon.

-   [Uso de metamarcações](#use-of-metatags)
-   [uso de Windows 8 estilo CSS](#use-of-windows-8-css-styling)
-   [Uso de cores e temas](#use-of-color-and-themes)
-   [Alinhamento](#alignment)
-   [Projetando para ajuste](#designing-for-snap)
-   [Projetando para uma experiência de logon rápida e fluida](#designing-for-a-fast-and-fluid-login-experience)
-   [Considerações sobre segurança](#security-considerations)
-   [Tópicos relacionados](#related-topics)

## <a name="use-of-metatags"></a>Uso de metamarcações

Usando metamarcações, o provedor "contoso social" pode especificar o título, o ícone e a cor do cabeçalho. No arquivo HTML de exemplo (WebAuthLogin.html), isso é feito usando o código a seguir.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



isso permite que Windows integre a presença do provedor de uma maneira proeminente no cabeçalho da interface do usuário, conforme realçado pela caixa vermelha na captura de tela a seguir. ![página de logon mostrando o cabeçalho da Contoso na interface do usuário](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>uso de Windows 8 estilo CSS

a folha de estilos ui-light. css fornecida é a Windows 8 folha de estilos usada pelos aplicativos da loja Windows. ele define Windows o estilo de aplicativo da loja para controles de tipografia e padrão, como botões, caixas de texto, hiperlinks e caixas de seleção para garantir que eles sejam amigáveis para toque. ao criar e personalizar páginas de autorização da web para Windows 8, incentivamos você a usar essa folha de estilo como está e a atualizar, conforme necessário, desde que sua página da web ainda siga as práticas recomendadas da mesma maneira.

por exemplo, se você tiver uma folha de estilos especial para o que os hiperlinks devem parecer na sua página da web, é bom ser elaborado para garantir que o estilo que você fornece seja amigável de toque da mesma forma que os hiperlinks padrão do Windows 8. isso é essencial para a base de consumidores usando Windows 8 em seus dispositivos de toque.

## <a name="use-of-color-and-themes"></a>Uso de cores e temas

Este exemplo demonstra um uso muito elaborado de cores de algumas maneiras diferentes.

-   Plano de fundo branco da página da Web. Como você pode ver na captura de tela anterior, a página da Web é hospedada dentro de uma superfície branca que abrange a largura do ecrã. Para garantir que a página da Web se integre com a superfície, é recomendável que a página da Web tenha um plano de fundo branco.
-   Colorir controles com base na sua cor de marca. O arquivo CSS Theme-Colors. css fornece estilos para substituir as cores padrão dos controles na folha de estilo da interface do usuário-Light para coincidir com os controles com a cor do cabeçalho. Por exemplo, na captura de tela a seguir, os botões e hiperlinks assumem cores derivadas da cor do cabeçalho. ![captura de tela dos botões e do texto com a mesma cor que o cabeçalho](images/wab-figure11.png)
-   Cor do cabeçalho. O uso da cor da marca da Contoso no cabeçalho cria uma personalidade unificada para a marca do provedor na interface do usuário do sistema.

## <a name="alignment"></a>Alinhamento

A página da Web não tem nenhum preenchimento à esquerda ou à direita para permitir o alinhamento tipográfico com o título no cabeçalho à esquerda e o ícone no cabeçalho à direita.

Você também observará que os botões estão sempre alinhados na parte inferior direita na página da Web (e alinhados à direita com o ícone no cabeçalho). essa é uma prática recomendada, pois Windows 8 usuários estarão acostumados com fluxos de caixa de diálogo semelhantes com botões no canto inferior direito.

## <a name="designing-for-snap"></a>Projetando para ajuste

Na imagem a seguir, você pode ver as páginas de logon e permissões no estado de ajuste.

![exibição de ajuste da tela de logon ](images/wab-figure12.png) . ![exibição de ajuste da página de permissões ](images/wab-figure13.png)

No arquivo de exemplo UI-webauth. CSS, você pode ver o uso de consultas de mídia que otimizam o layout da página para ajuste de estado com base na largura disponível para a página da Web. O trecho de código incluído no escopo a seguir implementa o CSS adaptado para o estado de ajuste.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



em Windows 8, a largura do estado de ajuste é de 320 pixels. A página de autenticação da Web ocupa 260 pixels na interface do usuário acima. Estamos usando um valor de largura máxima com margem suficiente, portanto, o código de consulta de mídia do provedor não está associado à largura exata do estado de ajuste.

Ao personalizar seu aplicativo para o modo de exibição de ajuste, é importante que o usuário não perca nenhum contexto que tenha nas outras exibições da experiência de autenticação da Web (exibições completa, de preenchimento ou de botão), mas é importante reestruturar o layout e a hierarquia dos elementos na página para que as informações necessárias para manter o contexto sejam visíveis e interativas. Nós chamamos alguns exemplos de como a amostra destaca a página da Web para o estado de ajuste.

-   Por exemplo, para a página de logon no estado de ajuste, a propriedade Width do campo de texto de entrada (conforme especificado em UI-Light. css) foi substituída e definida como um valor numérico menor, de modo que o campo de texto não seja cortado horizontalmente.
-   Como outro exemplo, no estado de ajuste, o tamanho da fonte dos cabeçalhos H1 e H2 é reduzido para 20 pt e 11 pt de 42 pt e 20 pt, respectivamente. isso é feito de acordo com a rampa de tipo de Windows 8 e otimiza o texto para ser mais compacto no visor alterado.
-   Como outro exemplo, observe que os tamanhos dos ícones na página permissões são menores (compare com a página de exibição completa acima). Novamente, isso é feito para manter o contexto, ao mesmo tempo que troca ativos de design para aqueles mais ideais para o visor alterado.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Projetando para uma experiência de logon rápida e fluida

No início da criação desta página da Web, fizemos um jogo no chão de que uma coisa que essa página é melhor é uma experiência de logon rápida e fluida. Assim, a interface do usuário que é mais proeminente no fluxo é o campo nome de usuário e senha na página de logon para uma experiência de entrada de credenciais rápida. Enquanto identificamos que há outros cenários comuns, como recuperação de senha, e referência de declarações de privacidade, a rica experiência da Web é um lugar melhor para essas experiências. Para todos os fluxos não relacionados à experiência segura da autenticação na Web, é recomendável navegar pelo usuário para o navegador. Isso é mostrado no arquivo HTML de exemplo (WebAuthLogin.html) da seguinte maneira: `<meta name="mswebdialog-newwindowurl" content="*" />` isso abre todas as páginas da Web vinculadas da página logon ou permissões no navegador padrão do usuário, em que o usuário pode concluir esses fluxos e, em seguida, retornar ao aplicativo para fazer logon.

## <a name="security-considerations"></a>Considerações de segurança

Os artigos a seguir fornecem diretrizes para escrever código C++ seguro.

-   [Práticas recomendadas de segurança para C++](/cpp/security/security-best-practices-for-cpp)
-   [Padrões & práticas de segurança diretrizes para aplicativos](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações para o desenvolvimento de páginas da Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Perguntas frequentes sobre o agente de autenticação da Web](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
