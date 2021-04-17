---
title: Sobre os controles de edição avançados
description: Esta seção apresenta controles de edição avançados.
ms.assetid: ab9dcdf4-a311-4159-8f37-e67e144f31f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95f6dc1cc1f37bf604e6c0a891f92cd20bb7af6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105755661"
---
# <a name="about-rich-edit-controls"></a>Sobre os controles de edição avançados

Os tópicos a seguir são discutidos nesta seção.

-   [Versões do rich edit](#versions-of-rich-edit)
    -   [Edição avançada versão 1,0](#rich-edit-version-10)
    -   [Edição avançada versão 2,0](#rich-edit-version-20)
    -   [Edição avançada versão 3,0](#rich-edit-version-30)
    -   [Edição avançada versão 4,1](#rich-edit-version-41)
-   [Funcionalidade de controle de edição sem suporte](#unsupported-edit-control-functionality)
-   [Teclas de atalho de edição avançada](#rich-edit-shortcut-keys)
-   [Tópicos relacionados](#related-topics)

## <a name="versions-of-rich-edit"></a>Versões do rich edit

A especificação original para controles de edição avançados é Microsoft Rich Edit 1,0; a especificação atual é Microsoft rich edit 4,1. Cada versão do Rich Edit é um superconjunto do anterior, exceto que apenas as compilações asiáticas do Microsoft Rich Edit 1,0 têm uma opção de texto vertical. Antes de criar um controle de edição rico, você deve chamar a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para verificar qual versão do Microsoft rich edit está instalada.

A tabela a seguir mostra qual DLL corresponde a qual versão do rich edit. Observe que o nome do arquivo não foi alterado da versão 2,0 para a versão 3,0. Isso permite que a versão 2,0 seja atualizada para a versão 3,0 sem interromper o código existente.



| Versão de edição avançada | DLL          | Classe de janela    |
|-------------------|--------------|-----------------|
| 1.0               | Riched32.dll | \_classe RichEdit |
| 2,0               | Riched20.dll | \_classe RichEdit |
| 3.0               | Riched20.dll | \_classe RichEdit |
| 4.1               | Msftedit.dll | \_classe MSFTEDIT |



 

### <a name="rich-edit-version-10"></a>Edição avançada versão 1,0

O Microsoft Rich Edit 1,0 inclui os seguintes recursos.



|                                                                                    |                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entrada e seleção de texto                                                           | A seleção e a entrada de texto da maioria padrão (controle de edição do sistema). Suporte à barra de seleção (a barra de seleção é uma área desmarcada à esquerda de cada parágrafo que, quando clicado, seleciona a linha). Opções de quebra automática de palavras e de palavras auto-seleção. Seleção de um único, duplo e de clique triplo. |
| Edição ANSI (conjunto de caracteres de byte único (SBCS) e conjunto de caracteres multibyte (MBCS)) | No entanto, não há nenhuma edição Unicode.                                                                                                                                                                                                                                                     |
| Conjunto básico de propriedades de formatação de caractere/parágrafo                             | Consulte [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) e [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat).                                                                                                                                                                                                                |
| Propriedades de formatação de caractere                                                    | Nome e tamanho da fonte, negrito, itálico, sublinhado sólido, tachado, protegido, link, deslocamento e cor do texto.                                                                                                                                                                                   |
| Propriedades de formatação de parágrafo                                                    | Recuo de início, recuo à direita, deslocamento de linha subsequente, marcador, alinhamento (esquerda, centro, direita) e guias.                                                                                                                                                                                    |
| Localizar avançar                                                                       | Inclui opções que não diferenciam maiúsculas de minúsculas e correspondências de palavras inteiras.                                                                                                                                                                                                                                   |
| Interface baseada em mensagem                                                            | Quase um superconjunto do conjunto de mensagens de controle de edição do sistema mais duas interfaces, [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) e [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback).                                                                                                              |
| Objetos inseridos                                                                   | Exige a colaboração do cliente com base nas interfaces [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) e [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .                                                                                                                                          |
| Suporte ao menu do botão direito                                                          | Usa a interface [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .                                                                                                                                                                                                                      |
| Edição de arrastar e soltar                                                              | Há suporte para a edição do tipo "arrastar e soltar".                                                                                                                                                                                                                                                       |
| Notificações                                                                      | [**WM \_**](/windows/desktop/menurc/wm-command) Mensagens de comando enviadas ao cliente, além de várias outras. Este é um superconjunto de notificações de controle comum.                                                                                                                                                 |
| Desfazer/refazer de nível único                                                             | Se comporta de forma semelhante ao controle de edição do sistema. A seleção de **desfazer** reverte a última ação, e essa ação torna-se a nova ação **refazer** .                                                                                                                                          |
| Texto vertical simples                                                               | (Somente compilações asiáticas).                                                                                                                                                                                                                                                                      |
| Suporte do IME (editor de método de entrada)                                                  | (Somente compilações asiáticas).                                                                                                                                                                                                                                                                      |
| Edição WYSIWYG usando métricas de impressora                                              | Esse recurso é necessário para o Microsoft WordPad, em particular.                                                                                                                                                                                                                              |
| Recortar/copiar/colar/transmitir/transmitir                                                  | Com texto sem formatação **( \_ texto CF**) ou Rich Text Format (RTF) com e sem objetos.                                                                                                                                                                                                        |
| Base de código C                                                                        | O código é escrito em C, que fornece uma base sólida e versátil.                                                                                                                                                                                                                |
| Compilações diferentes para scripts diferentes                                             | O Microsoft Rich Edit 1,0 aborda problemas de localização com compilações diferentes.                                                                                                                                                                                                              |



 

### <a name="rich-edit-version-20"></a>Edição avançada versão 2,0

O Microsoft rich edit 2,0 incorporou vários recursos adicionais, como o suporte para idiomas Unicode e asiático, as interfaces de desfazer vários níveis, Component Object Model (COM) e vários aprimoramentos de interface do usuário.

O Microsoft rich edit 2,0 inclui os seguintes recursos, além dos recursos fornecidos pelo [Microsoft rich edit 1,0](#rich-edit-version-10).



|                                               |                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unicode                                       | O Unicode facilita o esforço de tratamento de texto internacional. No entanto, é necessário um esforço para manter a compatibilidade com documentos não-Unicode existentes, ou seja, a capacidade de converter de/para texto sem formatação e Rich Text não Unicode.                                                                                                                                                             |
| Suporte internacional geral                 | Algoritmo de quebra de linha geral (extensão de regras kinsoku), vinculação de fonte simples, alternância de fonte de teclado.                                                                                                                                                                                                                                                                          |
| Suporte asiático                                 | O nível 2 (caixa de diálogo) e 3 (embutido) têm suporte em IMEs.                                                                                                                                                                                                                                                                                                                            |
| Encontre suporte para cima/localização                     | Há suporte para a pesquisa para frente e para trás.                                                                                                                                                                                                                                                                                                                                         |
| Suporte bidirecional                         | Isso está incluído no Microsoft rich edit 2,1                                                                                                                                                                                                                                                                                                                                          |
| Desfazer vários níveis                               | Uma arquitetura de desfazer extensível permite que o cliente participe do modelo de desfazer em todo o aplicativo.                                                                                                                                                                                                                                                                                         |
| Suporte ao mouse Magellan                        | Esse é o mouse com um cilindro para rolagem.                                                                                                                                                                                                                                                                                                                                       |
| Suporte a fontes duplas                             | O teclado pode alternar automaticamente as fontes quando a fonte ativa é inadequada para o teclado atual, por exemplo, caracteres kanji em Times New Roman.                                                                                                                                                                                                                            |
| Aplicação de fonte inteligente                              | A solicitação de alteração de fonte não aplica fontes ocidentais a caracteres asiáticos.                                                                                                                                                                                                                                                                                                                |
| Exibição aprimorada                              | Um bitmap fora da tela é usado quando várias fontes ocorrem na mesma linha. Isso permite, por exemplo, que a última letra da palavra legal não seja cortadosda.                                                                                                                                                                                                                           |
| Suporte à transparência                          | Também em modo sem janela.                                                                                                                                                                                                                                                                                                                                                             |
| Cores de seleção do sistema                       | Usado para selecionar o texto.                                                                                                                                                                                                                                                                                                                                                             |
| Reconhecimento automático de URL                     | Pode verificar um número de formatos de URL (por exemplo, http:)                                                                                                                                                                                                                                                                                                                           |
| Compatibilidade do Microsoft Word Edit UI          | Seleção, semântica do teclado-cursor.                                                                                                                                                                                                                                                                                                                                                  |
| EOP padrão do Word                             | A marca de fim de parágrafo (CR) também pode manipular retorno de carro/alimentação de linha (CR/LF) (retorno de carro, alimentação de linha).                                                                                                                                                                                                                                                                       |
| Texto sem formatação, bem como funcionalidade de Rich Text | Formato de caractere único e formato de parágrafo único.                                                                                                                                                                                                                                                                                                                                 |
| Controles de linha única e várias linhas            | Truncar no primeiro fim do parágrafo e nenhum WordWrap.                                                                                                                                                                                                                                                                                                                                  |
| Teclas de aceleração                              | Há suporte para teclas de aceleração.                                                                                                                                                                                                                                                                                                                                                      |
| Estilo da janela de senha                         | Os controles de edição de senha são fornecidos através de [**\_ getpasswordchar**](em-getpasswordchar.md) e em [**\_ SetPasswordChar**](em-setpasswordchar.md).                                                                                                                                                                                                                                 |
| Arquitetura escalonável                         | Para reduzir o tamanho da instância.                                                                                                                                                                                                                                                                                                                                                             |
| Operação e interfaces sem janelas           | Isso é fornecido por meio das interfaces [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) e [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .                                                                                                                                                                                                                                                                   |
| Interfaces duplas COM                           | Interfaces do modelo de objeto de texto (TOM).                                                                                                                                                                                                                                                                                                                                                  |
| CHARFORMAT2                                   | Espessura de fonte adicionada, cor do plano de fundo, identificador de localidade, tipo de sublinhado, sobrescrito e subscrito (além do deslocamento), efeito desabilitado. Somente para roundtripping RTF, foi adicionada a quantidade de espaço entre as letras, o tamanho de TWIP acima do par de kerning de caracteres, tipo de texto animado, vários efeitos: sombra da fonte/contorno, todas as letras maiúsculas, versalete, oculta, relevo, impressão e revisado. |
| PARAFORMAT2                                   | Espaço adicionado antes e depois e espaçamento de linha de palavra. Somente para roundtripping RTF, adição de peso/estilo de sombreamento, numeração inicial/estilo/guia, espaço de borda/largura/lados, alinhamento de tabulação/preenchimentos, vários efeitos de parágrafo do Word: parágrafo DPE, manter, manter próximo, página-quebra-antes, número de linha, n º de controle, não, não-hifen, lado a lado.                                         |
| Mais roundtripping RTF                        | Todas as propriedades Word FormatFont e FormatParagraph.                                                                                                                                                                                                                                                                                                                           |
| Estabilidade e estabilização de código              | Exemplos: validação de parâmetro e objeto, invariáveis de função, protetores de reentrância, estabilização de objeto.                                                                                                                                                                                                                                                                             |
| Infraestrutura de teste forte                 | Incluindo testes de regressões extensivos.                                                                                                                                                                                                                                                                                                                                               |
| desempenho aprimorado                          | Conjunto de trabalho menor, tempos de carregamento e de reexibição mais rápidos e assim por diante.                                                                                                                                                                                                                                                                                                                     |
| Base de código C++                                 | O código é escrito em C++, que fornece uma base sólida para criar o Microsoft Rich Edit 3,0.                                                                                                                                                                                                                                                                             |



 

Com algumas exceções, o Microsoft rich edit 2,0 usa as mesmas funções, estruturas e mensagens que o Microsoft Rich Edit 1,0. No entanto, observe as seguintes diferenças:

-   O nome da classe de janela do Microsoft Rich Edit 1,0 é **RichEdit**. O Microsoft rich edit 2,0 tem as classes de janela ANSI e Unicode **RichEdit20A** e **RichEdit20W,** respectivamente. Para especificar a classe de janela de edição avançada apropriada, use a \_ constante da classe RichEdit, que o arquivo RichEdit. h define dependendo da definição do sinalizador de compilação Unicode.
-   No Microsoft rich edit 2,0, se você criar um controle de edição Rich Unicode (um que espera mensagens de texto Unicode), deverá especificar apenas dados Unicode em qualquer mensagem de janela enviada ao controle. Da mesma forma, se você criar um controle de edição Rich ANSI, envie somente os dados ANSI ou DBCS (conjunto de caracteres de byte duplo). Você pode usar a função [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) para determinar se um controle de edição rico usa mensagens de texto Unicode. Observe que as interfaces COM de edição rica usam texto Unicode, a menos que encontrem um argumento de página de código.
-   O Microsoft Rich Edit 1,0 usou combinações de caracteres CR/LF para marcadores de parágrafo. O Microsoft rich edit 2,0 usou apenas um caractere de retorno de carro (' \\ r '). O Microsoft Rich Edit 3,0 usa apenas um caractere de retorno de carro, mas pode emular o Microsoft Rich Edit 1,0 nesse aspecto.
-   O Microsoft rich edit 2,0 introduziu as novas mensagens a seguir. 

    | Mensagem                                           | Descrição                                                             |
    |---------------------------------------------------|-------------------------------------------------------------------------|
    | [**em \_ AUTOURLDETECT**](em-autourldetect.md)     | Habilita ou desabilita a detecção automática de URL.                            |
    | [**em \_ refazer**](em-canredo.md)                 | Determina se há alguma ação na fila de restauração.             |
    | [**em \_ GETIMECOMPMODE**](em-getimecompmode.md)   | Recupera o modo do IME (editor de método de entrada) atual.                   |
    | [**em \_ GETlangoptions**](em-getlangoptions.md)   | Recupera opções de suporte a IME e idioma asiático.                   |
    | [**em \_ refazer**](em-getredoname.md)         | Recupera o nome do tipo da próxima ação na fila de restauração.           |
    | [**em \_ GETtextmode**](em-gettextmode.md)         | Recupera o modo de texto ou o nível de desfazer.                                  |
    | [**em \_ GETundoname**](em-getundoname.md)         | Recupera o nome do tipo da próxima ação na fila de desfazer.           |
    | [**em \_ refazer**](em-redo.md)                       | Refaz a próxima ação na fila de restauração.                               |
    | [**em \_ SETlangoptions**](em-setlangoptions.md)   | Define opções de suporte a IME e idioma asiático.                        |
    | [**em \_ SETtextmode**](em-settextmode.md)         | Define o modo de texto ou o nível de desfazer.                                       |
    | [**em \_ SETUNDOLIMIT**](em-setundolimit.md)       | Define o número máximo de ações na fila de desfazer.                   |
    | [**em \_ STOPGROUPTYPING**](em-stopgrouptyping.md) | Interrompe o agrupamento de ações de digitação consecutivas na ação de desfazer atual. |

    

     

-   O Microsoft rich edit 2,0 introduziu as novas estruturas a seguir. 

    | Estrutura                          | Descrição                                      |
    |------------------------------------|--------------------------------------------------|
    | [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) | Contém informações sobre a formatação de caracteres. |
    | [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) | Contém informações sobre a formatação de parágrafo. |

    

     

-   As mensagens a seguir têm suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0. Eles não têm suporte em nenhuma versão posterior do rich edit.

    [**em \_ CONVPOSITION**](em-convposition.md)

    [**em \_ GETIMECOLOR**](em-getimecolor.md)

    [**em \_ GETIMEOPTIONS**](em-getimeoptions.md)

    [**em \_ GETpontuation**](em-getpunctuation.md)

    [**em \_ GETwordwrapmode**](em-getwordwrapmode.md)

    [**em \_ SETIMECOLOR**](em-setimecolor.md)

    [**em \_ SETIMEOPTIONS**](em-setimeoptions.md)

    [**em \_ SETpontuation**](em-setpunctuation.md)

    [**em \_ SETwordwrapmode**](em-setwordwrapmode.md)

### <a name="rich-edit-version-30"></a>Edição avançada versão 3,0

O Microsoft Rich Edit 3,0 é uma DLL única, escalonável e em todo o mundo que oferece alto desempenho e compatibilidade com o Word em um pacote pequeno. Os novos recursos do Microsoft Rich Edit 3,0 incluem texto mais rico, zoom, associação de fontes, suporte mais potente ao IME e suporte avançado a scripts complexos (bidirecional, Índico e tailandês).

O Microsoft Rich Edit 3,0 inclui os seguintes recursos, além dos recursos fornecidos pela [versão de edição avançada 2,0](#rich-edit-version-20).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Zoom</td>
<td>O fator de zoom é fornecido por uma taxa.</td>
</tr>
<tr class="even">
<td>Numeração de parágrafos (nível único)</td>
<td>Alfabeto numérico, superior e inferior, ou algarismo romano.</td>
</tr>
<tr class="odd">
<td>Tabelas simples</td>
<td>É possível excluir e inserir linhas, mas não redimensionar nem quebrar dentro de células. Com a tipografia avançada ativada (consulte <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>), o Microsoft Rich Edit 3,0 pode alinhar colunas centralizadas ou esvaziadas à direita e incluir decimais. As células são simuladas por guias, portanto, as guias de texto e retornos de carro são substituídos por espaços em branco.</td>
</tr>
<tr class="even">
<td>Estilos normais e de título</td>
<td>O estilo normal interno e os estilos de título de 1 a 9 são compatíveis com as interfaces <a href="em-setparaformat.md"><strong>EM_SETPARAFORMAT</strong></a> e Tom ( <a href="text-object-model.md">modelo de objeto de texto</a> ).</td>
</tr>
<tr class="odd">
<td>Mais tipos de sublinhado</td>
<td>Tracejado, tracejado-ponto, traço-ponto-ponto e sublinhado de ponto foi adicionado.</td>
</tr>
<tr class="even">
<td>Cor do sublinhado</td>
<td>O texto sublinhado pode ser marcado com uma das 15 opções de documento para as cores de sublinhado.</td>
</tr>
<tr class="odd">
<td>Texto oculto</td>
<td>Marcado pelo atributo CHARFORMAT2. Útil para roundtripping (gravando em um arquivo que foi lido) de informações que normalmente não deveriam ser exibidas.</td>
</tr>
<tr class="even">
<td>Mais teclas de acesso padrão</td>
<td>Essas teclas de acesso funcionam da mesma forma que as do Word. Por exemplo, teclas mortas de ênfase Europeia (somente teclados dos EUA). Tecla de acesso de número (CTRL + L) percorre as opções de numeração disponíveis, começando com marcador.</td>
</tr>
<tr class="odd">
<td>HexToUnicode IME</td>
<td>Permite que um usuário converta entre hexadecimal e Unicode usando teclas de acesso.</td>
</tr>
<tr class="even">
<td>Aspas inglesas</td>
<td>Esse recurso é alternado e desativado por CTRL + ALT + ' para teclados norte-americanos.</td>
</tr>
<tr class="odd">
<td>Hifens suaves</td>
<td>Para texto sem formatação, use 0xAD. Para RTF, use \- .</td>
</tr>
<tr class="even">
<td>Cursor de itálico</td>
<td>Além disso, o cursor do mouse muda para uma mão quando sobre URLs.</td>
</tr>
<tr class="odd">
<td>Opção de tipografia avançada</td>
<td>O Microsoft Rich Edit 3,0 pode usar uma opção de tipografia avançada para a quebra de linha e a exibição (consulte <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>). Essa opção elegante foi adicionada principalmente para facilitar o tratamento de scripts complexos (bidirecional, Índico e tailandês). Além disso, vários aprimoramentos ocorrem para scripts simples. São exemplos:
<ul>
<li>Guias central, direita, decimal</li>
<li>Texto totalmente justificado</li>
<li>Sublinhar a média, que fornece um sublinhado uniforme mesmo quando o texto adjacente é executado com tamanhos de fonte diferentes.</li>
</ul></td>
</tr>
<tr class="even">
<td> Suporte a script complexo</td>
<td>O Microsoft Rich Edit 3,0 dá suporte a bidirecional (texto com árabe e/ou Hebraico misto com outros scripts), índicos (scripts indianos como Devangari) e texto em tailandês. Para dar suporte a esses scripts complexos, os componentes de tipografia avançada e de Uniscribe são usados.</td>
</tr>
<tr class="odd">
<td>Associação de fontes</td>
<td>O Microsoft Rich Edit 3,0 escolherá automaticamente uma fonte apropriada para caracteres que não pertençam ao carimbo do conjunto de caracteres atual. Isso é feito atribuindo conjuntos de caracteres a execuções de texto e associando fontes a esses conjuntos de caracteres. Para obter mais informações, consulte <a href="using-rich-edit-controls.md">Associação de fonte</a>.</td>
</tr>
<tr class="even">
<td>Opções de leitura/gravação de texto sem formatação específicas para conjuntos de caracteres</td>
<td>Isso permite a leitura de um arquivo usando um conjunto de caracteres e a gravação com um conjunto de caracteres diferente.</td>
</tr>
<tr class="odd">
<td>UTF-8 RTF</td>
<td>Isso é recomendado para recortar, copiar e colar operações. Esse formato de arquivo é mais compacto do que o RTF comum, mais rápido e compatível com Unicode.</td>
</tr>
<tr class="even">
<td>Suporte a Microsoft Office 9 IME (IME98)</td>
<td>Essa funcionalidade de IME mais potente foi separada em um módulo independente. Os recursos incluem:
<ul>
<li>Reconversão nas versões anteriores, o usuário precisava excluir a cadeia de caracteres final primeiro e, em seguida, digitar uma nova cadeia de caracteres para obter o candidato correto. Esse novo recurso permite que o usuário converta a cadeia de caracteres final de volta no modo de composição, permitindo, assim, a fácil seleção de uma cadeia de caracteres candidata diferente.<br/></li>
<li>Feed de documentos esse recurso fornece IME98 com o texto para o parágrafo atual, o que ajuda a IME98 a executar uma conversão mais precisa durante a digitação.<br/></li>
<li>Operação do mouse esse recurso fornece um melhor controle sobre as janelas do candidato e da interface do usuário durante a digitação.<br/></li>
<li>Posição do cursor esse recurso fornece as informações atuais de cursor e linha, que IME98 usa para posicionar janelas de interface do usuário (por exemplo, uma lista de candidatos).<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Suporte ao Gerenciador de método de entrada ativo (IMM)</td>
<td>Os usuários podem invocar o objeto ativo do IMM, que permite aos usuários inserir caracteres asiáticos em sistemas norte-americanos.</td>
</tr>
<tr class="even">
<td>Suporte do HexToUnicode</td>
<td>Os usuários podem converter entre notação hexadecimal e Unicode usando teclas de acesso.</td>
</tr>
<tr class="odd">
<td>Mais roundtripping RTF</td>
<td>O texto RTF que é lido em de um arquivo será gravado de volta intacto.</td>
</tr>
<tr class="even">
<td>Modo de compatibilidade 1,0 aprimorado</td>
<td>O Microsoft Rich Edit 3,0 pode emular o comportamento do Microsoft Rich Edit 1,0. Por exemplo, é possível alterar entre MBCS e os mapeamentos de CP (posição de caracteres Unicode).</td>
</tr>
<tr class="odd">
<td>Aumento do controle de congelamento</td>
<td>A exibição pode ser congelada em várias chamadas à API e, em seguida, descongelada para exibir as atualizações.</td>
</tr>
<tr class="even">
<td>Maior controle de desfazer</td>
<td>Desfazer pode ser suspenso e retomado (um requisito do IME).</td>
</tr>
<tr class="odd">
<td>Aumentar/diminuir tamanho da fonte</td>
<td>Aumenta ou diminui o tamanho da fonte para um dos seis valores padrão (12, 28, 36, 48, 72 e 80 pontos).</td>
</tr>
</tbody>
</table>



 

### <a name="rich-edit-version-41"></a>Edição avançada versão 4,1

A classe Window para Microsoft rich edit 4,1 é a \_ classe MSFTEDIT. Os novos recursos do Microsoft rich edit 4,1 incluem hifenização, rotação de página e suporte a TSF (estrutura de serviços de texto).

O Microsoft rich edit 4,1 inclui os seguintes recursos, além dos recursos fornecidos pela [versão de edição avançada 3,0](#rich-edit-version-30).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Hifenização</td>
<td>A hifenização é suportada por meio das seguintes APIs: <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a>, <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>e <a href="em-gethyphenateinfo.md"><strong>EM_GETHYPHENATEINFO</strong></a>.</td>
</tr>
<tr class="even">
<td>Rotação de página</td>
<td>Há suporte para layout de cima para baixo e de baixo para cima por meio de <a href="em-setpagerotate.md"><strong>EM_SETPAGEROTATE</strong></a> e <a href="em-getpagerotate.md"><strong>EM_GETPAGEROTATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>Suporte à estrutura de serviços de texto</td>
<td><ul>
<li>Para ativar o TSF e alguns recursos de TSF, use os seguintes estilos em <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a>: SES_USECTF, SES_CTFALLOWEMBED, SES_CTFALLOWPROOFING e SES_CTFALLOWSMARTTAG.</li>
<li>Para definir e obter a tendência do modo TSF, use <a href="em-setctfmodebias.md"><strong>EM_SETCTFMODEBIAS</strong></a> e <a href="em-getctfmodebias.md"><strong>EM_GETCTFMODEBIAS</strong></a>.</li>
<li>Para definir e obter o status do teclado do TSF, use <a href="em-setctfopenstatus.md"><strong>EM_SETCTFOPENSTATUS</strong></a> e <a href="em-getctfopenstatus.md"><strong>EM_GETCTFOPENSTATUS</strong></a>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Suporte a IME adicional</td>
<td><ul>
<li>Para definir e obter a tendência do modo IME, use <a href="em-setimemodebias.md"><strong>EM_SETIMEMODEBIAS</strong></a> e <a href="em-getimemodebias.md"><strong>EM_GETIMEMODEBIAS</strong></a>.</li>
<li>Para obter as propriedades e os recursos do IME, use <a href="em-getimeproperty.md"><strong>EM_GETIMEPROPERTY</strong></a>.</li>
<li>Para obter o texto de composição do IME, use <a href="em-getimecomptext.md"><strong>EM_GETIMECOMPTEXT</strong></a>.</li>
<li>Para determinar se a localidade é uma localidade do leste asiático, use <a href="em-isime.md"><strong>EM_ISIME</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Configurações de <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a> adicionais</td>
<td>Além das configurações de TSF, há novas configurações que excluem IMEs, definem o fluxo de texto bidirecional, usam fontes draftmode e muito mais.</td>
</tr>
<tr class="even">
<td>Configurações de <a href="em-setcharformat.md"><strong>EM_SETCHARFORMAT</strong></a> adicionais</td>
<td>Novos sinalizadores permitem que o cliente defina os tamanhos de fonte e fonte padrão para um determinado LCID ou conjunto de caracteres, para definir a fonte padrão do controle, para impedir que a alternância de teclado corresponda à fonte e muito mais.</td>
</tr>
<tr class="odd">
<td>Restringindo a entrada para texto ANSI</td>
<td>Usar <a href="/windows/win32/api/richedit/ne-richedit-textmode"><strong>TM_SINGLECODEPAGE</strong></a> em <a href="em-settextmode.md"><strong>EM_SETTEXTMODE</strong></a> impede que a entrada Unicode Insira um controle de edição rico.</td>
</tr>
<tr class="even">
<td>Notificação de palavra-chave RTF sem suporte</td>
<td><a href="en-lowfirtf.md">EN_LOWFIRTF</a> avisa um aplicativo quando há uma palavra-chave RTF sem suporte.</td>
</tr>
<tr class="odd">
<td>Suporte a idiomas adicionais</td>
<td>Os idiomas adicionais incluem armênio, divehi, télugo e outros.</td>
</tr>
<tr class="even">
<td>Suporte de tabela aprimorado</td>
<td>Os recursos incluem: encapsulamento dentro de células, tratamento aprimorado via RTF e navegação aprimorada.</td>
</tr>
<tr class="odd">
<td>ES_VERTICAL</td>
<td>Há suporte para o estilo de janela <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> .</td>
</tr>
<tr class="even">
<td>Suporte a <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a></td>
<td>Para enviar ou postar caracteres Unicode para janelas ANSI, use <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a>. É equivalente a <a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a>, mas usa (UTF)-32.</td>
</tr>
</tbody>
</table>



 

## <a name="unsupported-edit-control-functionality"></a>Funcionalidade de controle de edição sem suporte

Os controles de edição avançados dão suporte à maioria dos controles de edição de várias linhas, mas não a todas. Esta seção lista as mensagens de controle de edição e os estilos de janela que *não* são suportados pelos controles de edição avançados.

As mensagens a seguir são processadas por controles de edição, mas *não* por controles de edição avançados.



| Mensagem sem suporte                         | Comentários                                                                                                                    |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**em \_ FMTLINES**](em-fmtlines.md)         | Não há suporte.                                                                                                              |
| [**em \_ GEThandle**](em-gethandle.md)       | Os controles de edição avançados não armazenam texto como uma matriz simples de caracteres.                                                       |
| [**em \_ GETIMESTATUS**](em-getimestatus.md) | Não há suporte.                                                                                                              |
| [**em \_ GETmargins**](em-getmargins.md)     | Não há suporte.                                                                                                              |
| [**\_ONhandle**](em-sethandle.md)       | Os controles de edição avançados não armazenam texto como uma matriz simples de caracteres.                                                       |
| [**em \_ SETIMESTATUS**](em-setimestatus.md) | Não há suporte.                                                                                                              |
| [**\_SETmargins**](em-setmargins.md)     | Com suporte no Microsoft Rich Edit 3,0.                                                                                       |
| [**em \_ SETRECTNP**](em-setrectnp.md)       | Não há suporte.                                                                                                              |
| [**\_ONtabstops**](em-settabstops.md)   | Em vez disso, a mensagem em [**\_ SETPARAFORMAT**](em-setparaformat.md) é usada. Com suporte no Microsoft Rich Edit 3,0.<br/> |
| [**CTLCOLOR do WM \_**](/windows/desktop/DevNotes/wm-ctlcolor-)    | Em vez disso, a mensagem em [**\_ SETBKGNDCOLOR**](em-setbkgndcolor.md) é usada.                                                  |
| [**WM \_ GETfont**](/windows/desktop/winmsg/wm-getfont)        | Em vez disso, a mensagem em [**\_ GETCHARFORMAT**](em-getcharformat.md) é usada.                                                  |



 

Os seguintes estilos de janela são usados com controles de edição de várias linhas, mas não com controles de edição avançados: [**es \_ minúsculas**](edit-control-styles.md), [**es \_ maiúsculas**](edit-control-styles.md)e [**es \_ OEMCONVERT**](edit-control-styles.md).

## <a name="rich-edit-shortcut-keys"></a>Teclas de atalho de edição avançada

Os controles de edição avançados dão suporte às seguintes teclas de atalho.



| simétricas                      | Operations                                                                                                                               | Comentários                                                                                                                                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Shift + Backspace           | Gerar um LRM/LRM em um teclado bidi                                                                                                    | Específico BiDi                                                                                                                                                                                                                  |
| Ctrl+Tab                  | Tab                                                                                                                                      |                                                                                                                                                                                                                                |
| CTRL + Clear                | Selecionar tudo                                                                                                                               |                                                                                                                                                                                                                                |
| CTRL + número de teclado 5         | Selecionar tudo                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+A                    | Selecionar tudo                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+E                    | Alinhamento centralizado                                                                                                                         |                                                                                                                                                                                                                                |
| Ctrl+J                    | Justificar alinhamento                                                                                                                        |                                                                                                                                                                                                                                |
| Ctrl+R                    | Alinhamento à direita                                                                                                                          |                                                                                                                                                                                                                                |
| Ctrl+L                    | Alinhamento à esquerda                                                                                                                           |                                                                                                                                                                                                                                |
| Ctrl+C                    | Copiar                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+V                    | Colar                                                                                                                                    |                                                                                                                                                                                                                                |
| Ctrl+X                    | Recortar                                                                                                                                      |                                                                                                                                                                                                                                |
| Ctrl+Z                    | Desfazer                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+Y                    | Refazer                                                                                                                                     |                                                                                                                                                                                                                                |
| CTRL + ' + ' (Ctrl + Shift + ' = ') | Sobrescrito                                                                                                                              |                                                                                                                                                                                                                                |
| CTRL + ' = '                  | Subscrito                                                                                                                                |                                                                                                                                                                                                                                |
| Ctrl+1                    | Espaçamento de linha = 1 linha.                                                                                                                   |                                                                                                                                                                                                                                |
| Ctrl+2                    | Espaçamento de linha = 2 linhas.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+5                    | Espaçamento de linha = 1,5 linhas.                                                                                                                |                                                                                                                                                                                                                                |
| CTRL + ' (apóstrofo)       | Acento agudo                                                                                                                             | Depois de pressionar a tecla de corte curto, pressione a letra apropriada (por exemplo, a, e ou u). Isso se aplica apenas a teclados em inglês, francês, alemão, italiano e espanhol.                                                         |
| CTRL + \` (grave)           | Acento grave                                                                                                                             | Consulte CTRL + ' comentários.                                                                                                                                                                                                           |
| Ctrl + ~ (til)            | Til de acento                                                                                                                             | Consulte CTRL + ' comentários.                                                                                                                                                                                                           |
| CTRL +; ponto e vírgula        | Trema de ênfase                                                                                                                            | Consulte CTRL + ' comentários.                                                                                                                                                                                                           |
| Ctrl + Shift + 6              | Acento circunflexo (acento circunflexo)                                                                                                                | Consulte CTRL + ' comentários.                                                                                                                                                                                                           |
| CTRL +, (vírgula)            | Acento cedilha                                                                                                                           | Consulte CTRL + ' comentários.                                                                                                                                                                                                           |
| Ctrl + Shift + ' (apóstrofo) | Ativar aspas inglesas                                                                                                                    |                                                                                                                                                                                                                                |
| Backspace                 | Se o texto estiver protegido, emita um aviso sonoro e não o exclua. Caso contrário, exclua o caractere anterior.                                                   |                                                                                                                                                                                                                                |
| Ctrl+Backspace            | Excluir palavra anterior. Isso gera um \_ código VK F16.                                                                                     |                                                                                                                                                                                                                                |
| F16                       | O mesmo que Backspace.                                                                                                                       |                                                                                                                                                                                                                                |
| Ctrl+Insert               | Copiar                                                                                                                                     |                                                                                                                                                                                                                                |
| Shift+Insert              | Colar                                                                                                                                    |                                                                                                                                                                                                                                |
| Inserir                    | Overwrite                                                                                                                                | O DBCS não substitui.                                                                                                                                                                                                       |
| Ctrl+Seta para a Esquerda           | Mover o cursor uma palavra para a esquerda.                                                                                                        | No teclado bidi, isso depende da direção do texto.                                                                                                                                                                   |
| Ctrl+Seta para a Direita          | Mover o cursor uma palavra para a direita.                                                                                                       | Consulte CTRL + comentários da seta para a esquerda.                                                                                                                                                                                                  |
| CTRL + SHIFT esquerda           | Alinhamento à esquerda                                                                                                                           | Em documentos BiDi, isso é para a ordem de leitura da esquerda para a direita.                                                                                                                                                                    |
| CTRL + SHIFT direita          | Alinhamento à direita                                                                                                                          | Em documentos BiDi, isso é para a ordem de leitura da direita para a esquerda.                                                                                                                                                                    |
| Ctrl+Seta para Cima             | Mover para a linha acima.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+Seta para Baixo           | Mova para a linha abaixo.                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+Home                 | Mover para o início do documento.                                                                                                   |                                                                                                                                                                                                                                |
| Ctrl+End                  | Vá até o final do documento.                                                                                                         |                                                                                                                                                                                                                                |
| Ctrl + Page up              | Mover uma página para cima.                                                                                                                        | Se estiver no SystemEditMode e no controle de linha única, não faça nada.                                                                                                                                                                      |
| Ctrl + Page Down            | Mover uma página para baixo.                                                                                                                      | Veja comentários Ctrl + Page up.                                                                                                                                                                                                     |
| Ctrl+Delete               | Exclua a próxima palavra ou os caracteres selecionados.                                                                                             |                                                                                                                                                                                                                                |
| Shift+Delete              | Recortar os caracteres selecionados.                                                                                                             |                                                                                                                                                                                                                                |
| Esc                       | Parar arrastar e soltar.                                                                                                                          | Ao fazer um arrastar e soltar de texto.                                                                                                                                                                                               |
| Alt + Esc                   | Alterar o aplicativo ativo.                                                                                                           |                                                                                                                                                                                                                                |
| Alt+X                     | Converte o valor hexadecimal Unicode que precede o ponto de inserção para o caractere Unicode correspondente.                             |                                                                                                                                                                                                                                |
| Alt + Shift + X               | Converte o caractere Unicode que precede o ponto de inserção para o valor hexadecimal Unicode correspondente.                             |                                                                                                                                                                                                                                |
| Alt + 0xXX (teclado numérico)     | Insere valores Unicode se xxx for maior que 255. Quando xxx é menor que 256, o texto do intervalo ASCI é inserido com base no teclado atual. | É necessário inserir valores decimais.                                                                                                                                                                                                     |
| Alt + Shift + Ctrl + F12        | Hex para Unicode.                                                                                                                          | Caso ALT + X já tenha sido usado para outro uso.                                                                                                                                                                                |
| Alt + Shift + Ctrl + F11        | O texto selecionado será apresentado para a janela do depurador e salvo em% temp% \\DumpFontInfo.txt.                                               | Somente para depuração (é necessário definir o sinalizador = 8 em Win.ini)                                                                                                                                                                                 |
| Ctrl+Shift+A              | Defina todos os limites.                                                                                                                            |                                                                                                                                                                                                                                |
| Ctrl+Shift+L              | Estilo de marcador emendar.                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+Shift+Seta para a Direita    | Aumentar o tamanho da fonte.                                                                                                                      | O tamanho da fonte é alterado por 1 ponto no intervalo 4PT-11pt; por 2points para 12 pt-28pt; Ele muda de 28pt-> 36pt-> 48pt-> 72pt-> 80PT; Ele é alterado por 10 pontos no intervalo 80PT-1630pt; o valor máximo é 1638. |
| Ctrl+Shift+Seta para a Esquerda     | Diminuir o tamanho da fonte.                                                                                                                      | Consulte Ctrl + Shift + comentários da seta para a direita.                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Controles de edição avançados sem janela](windowless-rich-edit-controls.md)
</dt> </dl>

