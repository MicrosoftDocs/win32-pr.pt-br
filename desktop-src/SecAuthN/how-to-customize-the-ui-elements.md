---
description: Uma página da Web personaliza a interface do usuário com o título, o ícone e a cor do cabeçalho usando as marcas de metadados definidas na página da Web.
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: Como personalizar os elementos da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19314f8e4c5d4944a500a0eef3aa0f75cd231b12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829461"
---
# <a name="how-to-customize-the-ui-elements"></a>Como personalizar os elementos da interface do usuário

Uma página da Web personaliza a interface do usuário com o título, o ícone e a cor do cabeçalho usando as marcas de metadados definidas na página da Web. Os desenvolvedores da Web podem usar <meta> marcas HTML para exibir a personalidade e a marca do provedor na interface do usuário do agente de autenticação da Web. Além disso, os desenvolvedores podem direcionar ações de usuário mais complexas, por exemplo, inscrever-se e recuperar senhas. O conceito é muito semelhante ao recurso Sites fixos do Windows Internet Explorer 9 e do Windows 7.

Além de personalizar a interface do usuário na área da página da Web, a página da Web também deve aproveitar os estilos dos controles do Windows 8, estar habilitado para toque e permitir que os links sejam abertos no navegador, quando apropriado.

Veja a seguir um exemplo de uma página da Web que aproveitou o modelo de personalização do agente de autenticação da Web. ![elementos da interface do usuário do agente de autenticação da Web](images/wab-figure7.png)

## <a name="instructions"></a>Instruções

### <a name="step-1-customize-the-icon"></a>Etapa 1: personalizar o ícone

A página da Web pode fornecer um ícone usando uma marca meta de mswebdialog.

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

O conteúdo é uma URL que pode ser uma página relativa ou absoluta. O esquema da URL pode ser HTTP ou HTTPS. O formato do arquivo deve ser PNG ou JPG. O tamanho da imagem deve ser 30x30 pixels. Se a imagem for do tamanho diferente, ela será reduzida ou verticalmente pelo sistema operacional para se ajustar ao espaço 30x30. A imagem deve ser projetada para renderizar bem quando dimensionada para até 140% e 180% para considerar as telas de resolução mais alta. Para testar diferentes fatores de dimensionamento, use o [aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) carregado no Visual Studio 11, que permite simular diferentes resoluções e fatores de dimensionamento usando as janelas do dispositivo do modo de design.

### <a name="step-2-customize-the-title-text"></a>Etapa 2: personalizar o texto do título

A página da Web pode fornecer o título usando a marca meta mswebdialog-title.

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

O título deve ser curto e deve refletir a marca do provedor (por exemplo, contoso).

### <a name="step-3-customize-the-header-color"></a>Etapa 3: personalizar a cor do cabeçalho

A página da Web pode fornecer a cor que representa sua identidade de marca a ser usada para o cabeçalho da caixa de diálogo usando a marca meta mswebdialog-header-Color.

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

A cor pode ser qualquer valor especificado aqui. No entanto, o agente de autenticação da Web ignorará qualquer valor de canal alfa. Com essa cor especificamente e com as cores usadas na página em geral, é recomendável seguir as mesmas cores usadas no aplicativo do Windows 8 do provedor se esse aplicativo existir.

> [!Note]  
> Os ícones e as cores são armazenados em cache por servidor no cliente depois que as marcas META são analisadas. Limpe o cache do cliente antes de iniciar a interface do usuário para que as alterações entrem em vigor. Para fazer isso, modifique as seguintes configurações do registro.

 

``` syntax
// Registry location under HKLM used for setting various AuthHost parameters.
#define AUTH_HOST_LOCAL_MACHINE_REGPATH \
    L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Image File Execution Options\\authhost.exe"
// MaxAge to use for downloading logo images
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_REG_VALUE_NAME \
    L"LogoImageMaxAgeSeconds"
// 24 hours
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_DEFAULT        \
    (24 * 60 * 60)
```

Depois que um ícone é baixado, ele não é selecionado novamente por 24 horas. Para testar com imagens de logotipo, defina a chave de registro acima com um valor mais baixo.

### <a name="step-4-customize-the-web-page"></a>Etapa 4: personalizar a página da Web

Além de personalizar a interface do usuário em toda a página da Web, os desenvolvedores também devem criar páginas da Web que são integradas à experiência geral do Windows 8. Isso inclui o uso de estilos recomendados, garantindo que as páginas da Web funcionem bem com dispositivos habilitados para toque e abram determinadas páginas da Web no navegador da Web.

-   Estilo

    É altamente recomendável usar o estilo recomendado aqui para criar uma experiência de usuário mais consistente nas páginas da Web do agente de autenticação da Web e outros componentes da interface do usuário do Windows 8. A página da Web deve usar um plano de fundo branco e nenhuma borda. Os botões como logon ou cancelar devem ser posicionados no canto inferior direito e usar a mesma cor que o cabeçalho. Por fim, como o agente de autenticação da Web fornece um botão voltar, é recomendável eliminar completamente um botão Cancelar da página da Web.

-   Habilitando toque

    A página da Web deve ser projetada com uma interação de usuário baseada em toque em mente. Para obter mais informações sobre como projetar para toque no Windows 8, consulte o tópico [design de interação de toque](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) .

-   Personalizando o destino dos hiperlinks

    O agente de autenticação da Web é ótimo para fornecer páginas da Web que exigem uma única ação do usuário, como páginas de autorização de logon ou de OAuth. No entanto, para fluxos de usuário mais complexos, como a criação da conta, a recuperação de uma senha perdida ou esquecida, a exibição de declarações de privacidade e assim por diante, em que o usuário deve investir algum tempo para compreender e concluir o fluxo, é recomendável que essas páginas sejam iniciadas no navegador preferencial do usuário para dar suporte à navegação completa e à navegação do REACH. Por padrão, o agente de autenticação da Web não permite que novas janelas do navegador sejam abertas a partir de uma página da Web (consulte a seção não há novas janelas por padrão para obter mais detalhes). No entanto, usando a marca meta, `mswebdialog-newwindowurl` a página da Web pode declarar quais URLs devem ser abertas no navegador.

    O `mswebdialog-newwindowurl` permite que a página da Web especifique uma URL ou parte da URL que o agente de autenticação da Web usará para corresponder (correspondência de cadeia de caracteres à esquerda) em relação a cada vez que for solicitado a abrir uma URL em uma nova janela usando o atributo de destino ou o método window. Open (). Se houver uma correspondência, a URL será aberta no navegador padrão do usuário. Se não houver nenhuma correspondência, o agente de autenticação da Web navegará até a URL em si (comportamento padrão). Por exemplo: `<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    No caso dessa marca meta, o agente de autenticação da Web abrirá o https://www.contoso.com/privacy/policy.html no navegador, mas navegará diretamente para https://www.contoso.com/termsofuse.html . Observe que os links que não tentam abrir em uma nova janela (por exemplo, links que não estão usando o atributo de destino ou o método window. Open ()) não são afetados por essa marca meta. O conteúdo é uma URL que pode ser uma página relativa ou absoluta. O esquema da URL pode ser HTTP ou HTTPS. Você deve definir `mswebdialog-newwindowurl` marcas meta para abranger links que não fazem parte do fluxo do usuário principal, como declarações de privacidade, formulários de inscrição e assim por diante. Se você der suporte ao logon com um provedor de autenticação de terceiros (por exemplo, provedores de OpenID), certifique-se de manter essas interações no agente de autenticação da Web. Para habilitar todos os links em sua página como seguros para serem abertos no navegador, use a sintaxe de estrela, como, `  <meta name="mswebdialog-newwindowurl" content="*"/>` Observe que o " \* " só pode ser usado exclusivamente e não pode ser combinado com outra URL, por exemplo, " https://www.contoso.com/\ *" não é uma sintaxe válida.

### <a name="step-5-rules-applied-to-all-meta-tags"></a>Etapa 5: regras aplicadas a todas as marcas meta

Quando o agente de autenticação da Web processa marcas meta, as seguintes regras se aplicam:

-   O efeito da marca meta persistirá em todas as páginas no mesmo domínio de segundo nível (por exemplo, contoso.com), a menos que outra marca meta de mesmo nome, mas um conteúdo diferente, seja encontrada.
-   Se várias marcas meta de mesmo nome forem encontradas na mesma página, o agente de autenticação da Web escolherá apenas uma delas e ignorará o restante. Qual marca meta específica é escolhida é indefinida.
    > [!Note]  
    > Essa regra não se aplica à `mswebdialog-newwindowurl` marca meta que permite várias instâncias na mesma página.

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações para o desenvolvimento de páginas da Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
