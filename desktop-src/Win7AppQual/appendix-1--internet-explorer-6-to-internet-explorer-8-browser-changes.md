---
description: A tabela a seguir descreve as alterações entre o Microsoft Internet Explorer 6 e o Windows Internet Explorer 8.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Alterações no navegador IE 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7abf978d2211a03b59a78847a66efc21f3213c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828508"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Apêndice 1: alterações no navegador do Internet Explorer 6 para o Internet Explorer 8

A tabela a seguir descreve as alterações entre o Microsoft Internet Explorer 6 e o Windows Internet Explorer 8.



Alterações de design do Internet Explorer 6 para o Internet Explorer 7

Alterações de design do Internet Explorer 7 para o Internet Explorer 8

$ {ROWSPAN2} $Internet Explorer versão $ {remover} $  

Verifique se há um código incorretamente para casos especiais sobre o Internet Explorer 6, o Windows Internet Explorer 7 ou o Internet Explorer 8 por meio [de detecção de cadeias de caracteres de agente de usuário, vetores de versões ou comentários condicionais](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85)).

-   Quando uma cadeia de UA (agente de usuário longo) encontra um servidor que aceita apenas cadeias de caracteres de UA mais curtas, os usuários veem [uma página de erro](https://www.enhanceie.com/ua.aspx).

<!-- -->

-   A exibição de compatibilidade no Internet Explorer 8, que é ativada por padrão para sites de intranet, envia uma cadeia de caracteres de agente do usuário do Internet Explorer 7. Para diferenciar entre o Internet Explorer 7 e o modo de exibição de compatibilidade, procure o novo [token Trident](/archive/blogs/ie/).

Atualizações de conformidade de padrões do $ {ROWSPAN3} $

-   Aplica-se aos [modos de documento especificados](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)).
-   O [modo de exibição de compatibilidade do Internet Explorer 8](/archive/blogs/ie/), que é ativado por padrão para sites de intranet, normalmente [reverte atualizações de padrões do Internet Explorer 7 para o Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).
-   Use o cabeçalho http [compatível com EmulateIE7 X-UA](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) ou o elemento **meta** para habilitar a exibição de compatibilidade em sites ou páginas da Web específicas.

$ {REMOVER} $  

Exceção de modo peculiares: você não precisa fazer alterações de conformidade de padrões para páginas da Web que especificam o DOCTYPE do modo peculiares (definindo a opção DOCTYPE de "conformidade com os padrões" como "desativado").

Aplicável ao modo de Padrões do Internet Explorer 7 ou modo "Estrito" e superiores:

-   Os [Prologs XML](/previous-versions/windows/internet-explorer/ie-developer/) na primeira linha do código-fonte não causam mais declarações DOCTYPE para falharem.
-   Caixa interseção de conteúdo de estouro de [modelo de box](/previous-versions/windows/internet-explorer/ie-developer/) e não aumenta mais automaticamente a div de caixa para ajustar o conteúdo.
-   Não há suporte para [determinados filtros CSS](/previous-versions/windows/internet-explorer/ie-developer/) (por exemplo, \* HTML, \_ sublinhado e/ \* \* /Comentário).
-   [Somente o elemento de objeto mais externo em objetos aninhados](/previous-versions/windows/internet-explorer/ie-developer/) é instanciado.
-   Os [aplicativos que dependem do elemento select](/previous-versions/windows/internet-explorer/ie-developer/) para obter um HWND para usar com APIs do Microsoft Win32 podem ser interrompidos porque o [elemento select](/archive/blogs/ie/) agora é um controle sem janela.
-   Não há suporte para o [CDF (formato de definição de canal)](/previous-versions/aa740486(v=msdn.10)) , em favor dos RSS feeds.
-   [XBM](/previous-versions/aa740486(v=msdn.10)), não há suporte para um formato de geração de imagens projetado para sistemas baseados em X.
-   [Marcas base](/previous-versions/aa740486(v=msdn.10)) fora do documento de cabeçalho não são permitidas.

Aplicável ao modo de Padrões do Internet Explorer 8 e superiores:

-   [Os elementos P não fechados](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) são fechados automaticamente quando são seguidos pelos elementos [**Table**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx), [**Form**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx), [**noframes**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx)ou [**noscript**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx) .
-   Não há suporte para [HTML malformado](/archive/blogs/ie/site-compatibility-and-ie8) , em favor da marcação válida bem formada.
-   Não há suporte para a sintaxe de [atributo "ClassName"](/archive/blogs/ie/site-compatibility-and-ie8) , em favor da sintaxe "Class".
-   [A coleção Attributes](/archive/blogs/ie/site-compatibility-and-ie8) não contém todos os atributos possíveis que o Windows Internet Explorer reconhece.
-   A [ordenação de atributo foi alterada](/archive/blogs/ie/site-compatibility-and-ie8), afetando a coleta de atributos, innerHTML e OuterHtml.
-   [GetElementById](/archive/blogs/ie/site-compatibility-and-ie8) diferencia maiúsculas de minúsculas e não pesquisa atributos de nome.
-   Não há suporte para [seletores de prefixo CSS genéricos](/archive/blogs/ie/site-compatibility-and-ie8) (isto é, v \\ : \* Syntax), em favor de nomes de marca explícitos.
-   Não há suporte para [expressões CSS](/archive/blogs/ie/site-compatibility-and-ie8) , em favor do suporte a CSS aprimorado ou lógica DHTML.
-   O código destinado a métodos personalizados de objetos JSON pode entrar em conflito com o [novo objeto JSON nativo](/archive/blogs/ie/site-compatibility-and-ie8) no Internet Explorer 8.
-   [As propriedades iniciais definidas](/archive/blogs/ie/site-compatibility-and-ie8) no objeto currentStyle retornam seu valor inicial.
-   Os [valores de propriedades não especificadas](/archive/blogs/ie/site-compatibility-and-ie8) no objeto de estilo de objeto currentStyle retornam uma cadeia de caracteres vazia (por exemplo, consulte o [menu ASP.net e](/archive/blogs/giorgio/) a postagem do blog de renderização do IE8 de saída).

<!-- -->

-   Para sites e aplicativos em que a acessibilidade é uma preocupação, atualize a [sintaxe do Aria em todos os modos de renderização do Internet Explorer](/archive/blogs/ie/).
-   Verifique a [lista completa de atualizações de CSS do Internet Explorer 6 para o Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Aprimoramentos de segurança

-   Aplicar independentemente do modo de documento.
-   Você pode desativar os recursos de segurança usando [política de grupo](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab).

<!-- -->

-   O bypass do [Window. Open](/previous-versions/aa740486(v=msdn.10)) para a janela. Close não é permitido.
-   A [proteção de cache de objeto](/previous-versions/windows/internet-explorer/ie-developer/) é habilitada por padrão, o que bloqueia o acesso a referências de objetos quando os usuários navegam para um novo domínio (aplica-se ao Internet Explorer 6 e versões posteriores no Windows XP com Service Pack 2 (SP2) e versões posteriores).
-   Os [scriptlets DHTML](/previous-versions/windows/internet-explorer/ie-developer/) são desabilitados por padrão.
-   [Os scripts que gravam na barra de status](/previous-versions/windows/internet-explorer/ie-developer/) são bloqueados.
-   A [criação de URL poderá falhar](/previous-versions/windows/internet-explorer/ie-developer/) se as URLs não atenderem às diretrizes RFC.
-   As [páginas HTTPS exibirão uma página de erro](/previous-versions/windows/internet-explorer/ie-developer/) se o site estiver configurado para SSLv2 somente, ou se o certificado de segurança do site estiver desatualizado ou inválido, tiver erros ou tiver codificações fracas.
-   Somente os [nomes de domínio internacionalizados codificados "Punycode"](/previous-versions/windows/internet-explorer/ie-developer/) têm suporte. Outros formatos como ANSI e UTF-8 são bloqueados.
-   [URLs de script entre domínios](/previous-versions/windows/internet-explorer/ie-developer/), navegação redirecionada em objetos dom e navegações de quadros são bloqueadas.
-   [Caixas de diálogo modais ou sem janela restrita](/previous-versions/aa740486(v=msdn.10)) que são criadas a partir do script podem parecer [um pouco maiores](/archive/blogs/ie/).
-   Os [protocolos não seguros](/previous-versions/aa740486(v=msdn.10)) View-Source, Gopher (no nível do Wininet) e Telnet não funcionam.

<!-- -->

-   O [Filtro XSS](/archive/blogs/ie/) está ativado por padrão, o que bloqueia os padrões de script que mais frequentemente se assemelham a ataques de XSS tipo 1, a menos que você os desabilite por meio de um cabeçalho HTTP de proteção X-XSS.
-   Não há suporte para ataques de comunicação entre documentos entre domínios, como o [script src](/archive/blogs/jscript/) , em favor dos [recursos xdm e XDR Ajax](/archive/blogs/ie/)mais seguros.
-   Os sites habilitados para AJAX que [manipulam manualmente o hash da URL](/previous-versions//cc891506(v=vs.85)) podem ser quebrados pela nova propriedade de navegação Window. Location. hash.
-   [Novos recursos do AJAX](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) como [xdm](/archive/blogs/ie/) têm [**Propriedades nativas**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) que podem entrar em conflito com as propriedades personalizadas existentes.
-   O [controle de carregamento de arquivo](/archive/blogs/ie/) envia apenas o caminho do arquivo, não o caminho completo, para o servidor.
-   O script ou código HTML que é entregue com um [ \* tipo MIME "Image/"](/archive/blogs/ie/) é impedido de ser executado.
-   [Navegar em um quadro de nível superior](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) para um site em um contexto de segurança diferente abre uma nova janela ou guia em vez de navegar dentro do quadro existente.
-   O [script codificado em UTF-7](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) é forçado na codificação do Windows-1252, o que pode causar a renderização de texto sem formatação.
-   As [páginas de "modo misto" http/https](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) exibem uma caixa de diálogo que usa como padrão a exibição de itens seguros (em comparação com o padrão não seguro anterior). Os usuários podem, por engano, [optar por bloquear elementos http](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0), como imagens-chave.
-   O [DEP/NX está ativado por padrão](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx), o que bloqueia determinados complementos (ou seja, controles ActiveX e objetos com) que são criados usando versões mais antigas do ATL da execução de código que está marcado como "não executável" na memória.
-   [O conteúdo retornado por um proxy da Web](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) será bloqueado se um túnel SSL não for estabelecido em resposta a uma solicitação de conexão ao servidor original.

Alterações de arquitetura

-   Aplicar independentemente do modo de documento ou de compatibilidade.

<!-- -->

-   O [modo protegido](/previous-versions/windows/internet-explorer/ie-developer/) é habilitado por padrão para [zonas de Internet, intranet e sites restritos](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85)). Esse modo [bloqueia as extensões de navegador que podem representar um risco de segurança](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) na execução e na [redução dos aplicativos de privilégio de acessar processos de privilégio mais altos](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85)), como o menu Iniciar, o painel de controle e o registro do Microsoft Windows (aplica-se ao Internet Explorer 7 e versões posteriores no Windows Vista e versões posteriores).

<!-- -->

-   [Atualização do modo protegido](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85)): a intranet é executada em nível de integridade médio (em vez de baixo) por padrão.
-   O [Internet Explorer livremente acoplado](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) pode bloquear complementos (ou seja, controles ActiveX e objetos com) que fazem um dos seguintes:
    -   Use as técnicas de hierarquia do Windows para localizar janelas de quadro e guia da interface do usuário (que agora são executadas em processos separados em diferentes níveis de integridade).
    -   Crie uma subclasse do quadro da interface do usuário (agora no nível de integridade médio) de um processo de guia de baixa integridade.
    -   Use técnicas de mensagens sem suporte entre o quadro da interface do usuário e as guias.



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Abordando a compatibilidade de aplicativos ao migrar para o Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
