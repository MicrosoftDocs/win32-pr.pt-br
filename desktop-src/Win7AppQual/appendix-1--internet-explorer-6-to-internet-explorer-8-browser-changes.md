---
description: A tabela a seguir descreve as alterações entre o Microsoft Internet Explorer 6 e Windows Internet Explorer 8.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Alterações no navegador do IE 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c775448d8eca55097b0121592c28ece0b2c347f4492e7a48b2d51d9ab688fa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680285"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Apêndice 1: Internet Explorer 6 para Internet Explorer do navegador 8

A tabela a seguir descreve as alterações entre o Microsoft Internet Explorer 6 e Windows Internet Explorer 8.



Alterações de design Internet Explorer 6 para Internet Explorer 7

Alterações de design Internet Explorer 7 para Internet Explorer 8

${ROWSPAN2}$Internet Explorer versioning${REMOVE}$  

Verifique se há código que incorretamente tem casos especiais em torno do Internet Explorer 6, Windows Internet Explorer 7 ou Internet Explorer 8 por meio de busca de cadeia de caracteres de agente do usuário, vetores de versões ou comentários [condicionais](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85)).

-   Quando uma cadeia de caracteres de agente do usuário (UA) longa encontra um servidor que aceita apenas cadeias de caracteres de UA mais curtas, os usuários veem [uma página de erro](https://www.enhanceie.com/ua.aspx).

<!-- -->

-   O Modo de Exibição de Compatibilidade no Internet Explorer 8, que é ligado por padrão para sites da intranet, envia uma cadeia Internet Explorer de agente de usuário 7. Para diferenciar entre Internet Explorer 7 e Modo de Exibição de Compatibilidade, procure o novo [token Trident](/archive/blogs/ie/).

Atualizações de conformidade de ${ROWSPAN3}$ Standards

-   Aplica-se [aos modos de documento especificados.](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85))
-   [Internet Explorer 8 Modo de Exibição de Compatibilidade modo](/archive/blogs/ie/), que está on por padrão para sites da intranet, normalmente reverte as atualizações de padrões do Internet Explorer 7 para [Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).
-   Use o cabeçalho HTTP compatível com [EmulateIE7 X-UA](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) ou o **meta** element para habilitar Modo de Exibição de Compatibilidade em sites ou páginas da Web específicas.

${REMOVE}$  

Exceção do modo Desintes: você não precisa fazer alterações de conformidade de padrões para páginas da Web que especificam o modo de características DOCTYPE (definindo a opção DOCTYPE "standards-compliance" como "off").

Aplicável ao modo de Padrões do Internet Explorer 7 ou modo "Estrito" e superiores:

-   [Os prólogos XML](/previous-versions/windows/internet-explorer/ie-developer/) na primeira linha do código-fonte não causam mais falha nas declarações DOCTYPE.
-   [O conteúdo de](/previous-versions/windows/internet-explorer/ie-developer/) estouro de modelo de caixa intersecções e não aumenta automaticamente o div de caixa para se ajustar ao conteúdo.
-   [Determinados filtros CSS](/previous-versions/windows/internet-explorer/ie-developer/) (por \* exemplo, \_ HTML, sublinhado e \* \* //comment) não têm suporte.
-   [Somente o elemento OBJECT mais externo em objetos aninhados](/previous-versions/windows/internet-explorer/ie-developer/) é instautado.
-   [Os aplicativos que dependem](/previous-versions/windows/internet-explorer/ie-developer/) do elemento SELECT para obter um HWND a ser usado com APIs do Microsoft Win32 podem se quebrar porque o [elemento SELECT](/archive/blogs/ie/) agora é um controle sem janelas.
-   [Não há suporte para CDF (Formato](/previous-versions/aa740486(v=msdn.10)) de Definição de Canal) em favor de feeds RSS.
-   [XBM](/previous-versions/aa740486(v=msdn.10)), um formato de imagens projetado para sistemas baseados em X, não tem suporte.
-   [Marcas BASE](/previous-versions/aa740486(v=msdn.10)) fora do documento HEAD não são permitidas.

Aplicável ao modo de Padrões do Internet Explorer 8 e superiores:

-   [Os elementos P semlos](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) são fechados automaticamente quando são seguidos pelos elementos [**TABLE**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx), [**FORM,**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx) [**NOFRAMES**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx) [**ou NOSCRIPT.**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx)
-   [Não há suporte para HTML](/archive/blogs/ie/site-compatibility-and-ie8) malformado, em favor de marcação válida e bem formada.
-   Não há suporte para a sintaxe de atributo ["className",](/archive/blogs/ie/site-compatibility-and-ie8) em favor da sintaxe "class".
-   [A coleção de](/archive/blogs/ie/site-compatibility-and-ie8) atributos não contém todos os atributos possíveis que Windows Internet Explorer reconhece.
-   [A ordenação de atributo alterou](/archive/blogs/ie/site-compatibility-and-ie8), afetando a coleção de atributos, innerHTML e outerHTML.
-   [GetElementById](/archive/blogs/ie/site-compatibility-and-ie8) faz o reconhecimento de minúsculas e não pesquisa atributos de nome.
-   Não há suporte para seletores de [prefixo CSS genéricos](/archive/blogs/ie/site-compatibility-and-ie8) (ou seja, v \\ : \* sintaxe), em favor de nomes de marca explícitos.
-   [Não há suporte para](/archive/blogs/ie/site-compatibility-and-ie8) expressões CSS, em favor do suporte de CSS aprimorado ou à lógica DHTML.
-   O código destinado a métodos de objeto JSON personalizados pode entrar em conflito com o novo objeto [JSON](/archive/blogs/ie/site-compatibility-and-ie8) nativo Internet Explorer 8.
-   [Desinetize as](/archive/blogs/ie/site-compatibility-and-ie8) propriedades iniciais no objeto currentStyle retornam seu valor inicial.
-   [Os valores de propriedades](/archive/blogs/ie/site-compatibility-and-ie8) não especificados no objeto de estilo de objeto currentStyle retornam uma cadeia de caracteres vazia (por exemplo, consulte a postagem no blog menu ASP.NET e problema de renderização [do IE8).](/archive/blogs/giorgio/)

<!-- -->

-   Para sites e aplicativos em que a acessibilidade é uma preocupação, atualize a sintaxe do ARIA em todos [os Internet Explorer de renderização.](/archive/blogs/ie/)
-   Verifique a [lista completa de atualizações css do Internet Explorer 6 para Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Aprimoramentos de segurança

-   Aplique independentemente do modo de documento.
-   Você pode desativar os recursos de segurança usando [Política de Grupo](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab).

<!-- -->

-   O [bypass window.opener](/previous-versions/aa740486(v=msdn.10)) para o prompt window.close não é permitido.
-   A proteção de [cache](/previous-versions/windows/internet-explorer/ie-developer/) de objetos é habilitada por padrão, o que bloqueia o acesso a referências de objetos quando os usuários navegam para um novo domínio (aplica-se ao Internet Explorer 6 e versões posteriores no Windows XP com Service Pack 2 (SP2) e versões posteriores).
-   [Os scriptlets DHTML](/previous-versions/windows/internet-explorer/ie-developer/) são desabilitados por padrão.
-   [Os scripts que escrevem na barra de status](/previous-versions/windows/internet-explorer/ie-developer/) são bloqueados.
-   [A criação de URL poderá falhar](/previous-versions/windows/internet-explorer/ie-developer/) se as URLs não atenderem às diretrizes de RFC.
-   [As páginas HTTPS](/previous-versions/windows/internet-explorer/ie-developer/) exibirão uma página de erro se o site estiver configurado apenas para SSLv2 ou se o certificado de segurança do site estiver desatualizado ou inválido, tiver erros ou tiver codificações fracas.
-   Há suporte apenas para nomes de domínio [internacionalizados codificados por "Punycode".](/previous-versions/windows/internet-explorer/ie-developer/) Outros formatos, como ANSI e UTF-8, são bloqueados.
-   [URLs de script entre domínios,](/previous-versions/windows/internet-explorer/ie-developer/)navegação redirecionada em objetos DOM e navegaçãos de quadro são bloqueadas.
-   [Caixas de diálogo modais ou sem modo](/previous-versions/aa740486(v=msdn.10)) criadas com o script podem parecer [um pouco maiores.](/archive/blogs/ie/)
-   [A fonte de exibição](/previous-versions/aa740486(v=msdn.10)) de protocolos não confiável, Gopher (no nível do WinINET) e Telnet não funcionam.

<!-- -->

-   O [filtro XSS](/archive/blogs/ie/) está em por padrão, o que bloqueia padrões de script que mais frequentemente se assemelham a ataques XSS do Tipo 1, a menos que você os desabilite por meio de um cabeçalho HTTP X-XSS-Protection.
-   Não há suporte para hacks de comunicação entre domínios e documentos cruzados, como [SCRIPT SRC,](/archive/blogs/jscript/) em favor de recursos mais seguros de [XDM e XDR AJAX.](/archive/blogs/ie/)
-   Sites habilitados para AJAX que [manipulam manualmente](/previous-versions//cc891506(v=vs.85)) o hash da URL podem ser desfeitos pela nova propriedade de navegação window.location.hash.
-   [Novos recursos do AJAX,](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) como [XDM, têm](/archive/blogs/ie/) [**propriedades nativas**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) que podem estar em conflito com as propriedades personalizadas existentes.
-   [O controle de upload](/archive/blogs/ie/) de arquivo envia apenas o caminho do arquivo, não o caminho completo, para o servidor.
-   O código HTML ou script que é entregue com um [tipo \* MIME "image/"](/archive/blogs/ie/) está impedido de ser executado.
-   [Navegar por um quadro](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) de nível superior para um site em um contexto de segurança diferente abre uma nova janela ou guia em vez de navegar dentro do quadro existente.
-   [O script codificado em UTF-7](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) é forçado Windows codificação-1252, o que pode causar renderização de texto sem-texto.
-   [As páginas HTTP/HTTPS de "modo misto"](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) exibem uma caixa de diálogo que tem como padrão exibir apenas itens seguros (em comparação com o padrão não seguro anterior). Os usuários podem optar por [bloquear por engano elementos HTTP,](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0)como imagens-chave.
-   [O DEP/NX](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx)está ligado por padrão, que bloqueia determinados complementos (ou seja, controles ActiveX e objetos COM) que são construídos usando versões mais antigas da ATL do código em execução marcado como "não executável" na memória.
-   [O conteúdo retornado por um proxy da Web](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) será bloqueado se um túnel SSL não for estabelecido em resposta a uma solicitação CONNECT para o servidor original.

Alterações de arquitetura

-   Aplique independentemente do documento ou modo de compatibilidade.

<!-- -->

-   [O Modo Protegido é](/previous-versions/windows/internet-explorer/ie-developer/) habilitado por padrão para [zonas de Internet, Intranet e Sites Restritos.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85)) Esse [](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) modo bloqueia as extensões do navegador que podem representar um risco de segurança de executar e reduzir os processos de [privilégio,](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85))como o menu Iniciar, o Painel de Controle e o Registro do Microsoft Windows (aplica-se ao Internet Explorer 7 e versões posteriores no Windows Vista e versões posteriores).

<!-- -->

-   [Atualização de modo protegido:](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85))a intranet é executado em nível de integridade médio (em vez de baixo) por padrão.
-   [Os Internet Explorer podem](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) bloquear complementos (ou seja, controles ActiveX e objetos COM) que fazem um dos seguintes:
    -   Use técnicas de hierarquia do Windows para localizar janelas de quadro e tabulação da interface do usuário (que agora são executados em processos separados em diferentes níveis de integridade).
    -   Crie uma subclasse do quadro da interface do usuário (agora no nível médio de integridade) de um processo de guia de baixa integridade.
    -   Use técnicas de mensagens sem suporte entre o quadro da interface do usuário e as guias.



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Abordando a compatibilidade de aplicativos ao migrar para o Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
