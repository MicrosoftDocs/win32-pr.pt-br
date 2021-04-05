---
title: Sobre o modelo de objeto de texto
description: Este tópico fornece uma visão geral de alto nível do TOM.
ms.assetid: e304ec18-ec2e-4ea7-91c6-6f6ab63b72ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b934aab1cbd3dca932b58e4aa99498843cb8cc97
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008478"
---
# <a name="about-text-object-model"></a>Sobre o modelo de objeto de texto

O TOM (modelo de objeto de texto) define um conjunto de interfaces de manipulação de texto com suporte em graus variados por várias soluções de texto da Microsoft, incluindo o controle rich edit. Este tópico fornece uma visão geral de alto nível do TOM. Ele aborda os tópicos a seguir.

-   [Objetos de TOM versão 2](#tom-version-2-objects)
-   [Convenções de interface TOM](#tom-interface-conventions)
-   [O tipo tomBool](#the-tombool-type)
-   [Acúmulo e compilação de matemática](#math-buildup-and-build-down)
-   [TOM RTF](#tom-rtf)
-   [Localizando Rich Text](#finding-rich-text)
-   [TOM de acessibilidade](#tom-accessibility)
    -   [Interface da tabela de objetos em execução](#interface-from-running-object-table)
    -   [Interface de mensagens de janela](#interface-from-window-messages)
    -   [Métodos orientados a acessibilidade](#accessibility-oriented-methods)
-   [Conjuntos de correspondência de caracteres](#character-match-sets)

## <a name="tom-version-2-objects"></a>Objetos de TOM versão 2

TOM versão 2 (TOM 2) estende o modelo de objeto de texto original; as novas interfaces são derivadas das antigas. A API de TOM atualizado inclui suporte para novas propriedades de formato de parágrafo e de caractere, um modelo de tabela, seleção múltipla e suporte a objetos embutidos para matemática e Ruby.

O objeto TOM 2 de nível superior é definido pela interface [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) , que tem métodos para criar e recuperar objetos inferiores na hierarquia de objetos. Para um processamento de texto simples simples, você pode obter um objeto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) de um objeto **ITextDocument2** e fazer mais tudo com isso. Se precisar adicionar formatação rich-text, você poderá obter objetos [**ITextFont2**](/windows/desktop/api/Tom/nn-tom-itextfont2) e [**ITextPara2**](/windows/desktop/api/Tom/nn-tom-itextpara2) de um objeto **ITextRange2** . **ITextFont2** fornece o equivalente em programação da caixa de diálogo formato-fonte do Microsoft Word e **ITextPara2** fornece o equivalente à caixa de diálogo formato de palavra-parágrafo.

Além desses três objetos de nível inferior, José 2 tem um objeto Selection ([**ITextSelection2**](/windows/win32/api/tom/nn-tom-itextselection2)), que é um objeto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) com realce de seleção e alguns métodos orientados por interface do usuário.

Os objetos de intervalo e seleção incluem métodos orientados por tela que permitem que os programas examinem texto na tela ou texto que podem ser rolados na tela. Esses recursos ajudam a tornar o texto acessível a pessoas com visão inemparelhada, por exemplo.

Cada interface que tem o sufixo 2 é herdada da interface correspondente sem o sufixo 2. Por exemplo, [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) herda de [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument).

Os objetos TOM 2 têm a seguinte hierarquia.

``` syntax
ITextDocument2         Top-level editing object
    ITextRange2        Primary text interface: a range of text
        ITextFont2     Character-attribute interface
        ITextPara2     Paragraph-attribute interface
        ITextRow       Table interface
    ITextSelection2    Screen highlighted text range
        ITextRange2    Selection inherits all range methods
    ITextDisplays      Displays collection (not yet defined)
    ITextStrings       Rich-text strings collection
    ITextStoryRanges2  Enumerator for stories in document
```

Um objeto [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) descreve um ou mais intervalos contíguos de texto chamados *histórias*. As histórias representam várias partes de um documento, como o texto principal do documento, cabeçalhos e rodapés, notas de rodapé, anotações e pads de rascunhos de texto rico. Uma história de bloco transitório é usada ao converter entre expressões matemáticas formatadas linearmente e um formulário interno. Uma história do bloco de rascunho também é usada ao salvar o conteúdo de um intervalo que é a origem da cópia atual quando o conteúdo está prestes a ser alterado.

Um objeto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) é definido por seus deslocamentos de posição de caractere inicial e final e um objeto de história. Ele não existe independentemente do seu objeto de história pai, embora seu texto possa ser copiado para a área de transferência ou para outros destinos. Um objeto de intervalo de texto é diferente da planilha e de outros objetos de intervalo, que são definidos por outros tipos de deslocamentos; por exemplo, linha/coluna ou posição de gráficos (x, y). Um objeto de intervalo de texto pode se modificar de várias maneiras, pode retornar uma duplicata de si mesmo, e pode ser commandado para copiar suas posições de caractere inicial e final e seu ponteiro de história para a seleção atual.

Um objeto Story explícito não é necessário, pois um objeto [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) sempre pode ser criado para representar uma determinada história. Em particular, o objeto [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) pode criar um objeto [**ITextStoryRanges**](/windows/desktop/api/Tom/nn-tom-itextstoryranges) para enumerar as histórias no documento em termos de intervalos com valores de posição de caractere inicial e final que descrevem histórias completas (como, 0 e **tomForward**).

Com um objeto [**ITextStoryRanges2**](/windows/desktop/api/Tom/nn-tom-itextstoryranges2) , um objeto de história explícito não é necessário, pois cada história é descrita por um objeto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) . Em particular, o objeto [**ITextDocument2**](/windows/desktop/api/tom/nn-tom-itextdocument2) pode criar um objeto [**ITextStoryRanges2**](/windows/desktop/api/tom/nn-tom-itextstoryranges2) para enumerar as histórias no documento em termos de intervalos com valores de posição de caractere inicial e final que descrevem histórias completas (como, 0 e **tomForward**).

A interface [**ITextRow**](/windows/desktop/api/Tom/nn-tom-itextrow) junto com os métodos [**ITextRange:: move**](/windows/desktop/api/Tom/nf-tom-itextrange-move) e [**ITextRange:: Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand) fornecem a capacidade de inserir, consultar e alterar tabelas.

## <a name="tom-interface-conventions"></a>Convenções de interface TOM

Todos os métodos TOM retornam valores **HRESULT** . Em geral, os métodos TOM retornam os valores padrão a seguir.

-   E \_ OUTOFMEMORY
-   E \_ INVALIDARG
-   E \_ NOTIMPL
-   E \_ FILENOTFOUND
-   E \_ ACCESSDENIED
-   E \_ falha
-   CO \_ E \_ lançado
-   NOERROR (igual a S \_ OK)
-   \_falso

Lembre-se de que se a instância de edição associada a um objeto TOM, como [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) , for excluída, o objeto Tom se tornará inútil e todos os seus métodos retornarão \_ e serão \_ liberados.

Além dos valores de retorno **HRESULT** , muitos métodos incluem parâmetros de saída, que são ponteiros usados para retornar valores. Para todas as interfaces, você deve verificar todos os parâmetros de ponteiro para garantir que eles sejam diferentes de zero antes de usá-los. Se você passar um valor nulo para um método que requer um ponteiro válido, o método retornará E \_ INVALIDARG. Os ponteiros de saída opcionais com valores nulos são ignorados.

Use métodos com prefixos Get e Set para obter e definir propriedades. As variáveis Booleanas usam **tomFalse** (0) para **false** e **tomTrue** (-1) para **true**.

As constantes de TOM são definidas no tipo de enumeração [**tomConstants**](/windows/win32/api/tom/ne-tom-tomconstants) e começam com o prefixo *Tom*, por exemplo, **tomWord**.

## <a name="the-tombool-type"></a>O tipo tomBool

Muitos métodos TOM usam um tipo especial de variável chamada "tomBool" para atributos de texto rico que têm Estados binários. O tipo tomBool é diferente do tipo **booliano** porque pode ter quatro valores: **tomTrue**, **tomFalse**, **tomToggle** e **tomUndefined**. Os valores **tomTrue** e **tomFalse** indicam true e false. O valor **tomToggle** é usado para alternar uma propriedade. O valor de **tomUndefined** , mais tradicionalmente chamado de NINCH, é um valor especial de ausência de entrada, sem alteração que funciona com longos, floats e **COLORREF** s. Para cadeias de caracteres, **tomUndefined** (ou NINCH) é representado pela cadeia NULL. Para operações de configuração de propriedade, o uso de **tomUndefined** não altera a propriedade de destino. Para operações de obtenção de propriedade, **tomUndefined** significa que os caracteres no intervalo têm valores diferentes (ele dá a caixa de seleção cinza nas caixas de diálogo de propriedade).

## <a name="math-buildup-and-build-down"></a>Acúmulo e compilação de matemática

Você pode usar o método [**ITextRange2:: BuildUpMath**](/windows/desktop/api/Tom/nf-tom-itextrange2-buildupmath) para converter expressões matemáticas formatadas linearmente em versões internas. O método [**ITextRange2:: linear**](/windows/desktop/api/Tom/nf-tom-itextrange2-linearize) faz a conversão oposta, chamada linearização ou desativada, para converter versões de expressões matemáticas de volta para o formato linear. A funcionalidade de compilação matemática é útil quando você precisa exportar texto sem formatação ou para habilitar determinados tipos de edição.

## <a name="tom-rtf"></a>TOM RTF

Em TOM, o Exchange de Rich Text pode ser realizado por conjuntos de chamadas de método explícitas ou por transferências de Rich Text no RTF (Rich Text Format). Esta seção fornece tabelas de palavras de controle RTF para propriedades de parágrafo e propriedades de caractere.

**Palavras de controle de parágrafo TOM RTF**

| Palavra de controle   | Significado                                                                                                                                                                                                                                                                        |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ Fi *n*      | Recuo de primeira linha (o padrão é zero).                                                                                                                                                                                                                                       |
| \\ manter        | Mantenha o parágrafo intacto.                                                                                                                                                                                                                                                         |
| \\ manter       | Continue com o próximo parágrafo.                                                                                                                                                                                                                                                  |
| \\ Li *n*      | Recuo à esquerda (o padrão é zero).                                                                                                                                                                                                                                             |
| \\ noline      | Nenhuma numeração de linha.                                                                                                                                                                                                                                                             |
| \\ nowidctlpar | Desative o controle viúva/órfão.                                                                                                                                                                                                                                                 |
| \\ pagebb      | Quebra a página antes do parágrafo.                                                                                                                                                                                                                                                   |
| \\ nominal         | Novo parágrafo.                                                                                                                                                                                                                                                                 |
| \\ pard        | Redefine para propriedades de parágrafo padrão.                                                                                                                                                                                                                                        |
| \\ QL          | Alinhado à esquerda (o padrão).                                                                                                                                                                                                                                                    |
| \\ QR          | Alinhado à direita.                                                                                                                                                                                                                                                                 |
| \\ QJ          | Justificado.                                                                                                                                                                                                                                                                     |
| \\ QC          | Centralizado.                                                                                                                                                                                                                                                                      |
| \\ ri *n*      | Recuo à direita (o padrão é zero).                                                                                                                                                                                                                                            |
| \\ s *n*       | Estilo *n*.                                                                                                                                                                                                                                                                     |
| \\ SA *n*      | Espaço após (o padrão é zero).                                                                                                                                                                                                                                             |
| \\ SB *n*      | Espaço antes (o padrão é zero).                                                                                                                                                                                                                                            |
| \\ SL *n*      | Se estiver ausente ou se *n*= 1000, o espaçamento de linha será determinado pelo caractere mais alto na linha (espaçamento de linha única); Se *n*> zero, pelo menos esse tamanho será usado; Se *n* for < zero, exatamente \| *n* \| será usado. O espaçamento de linha é espaçamento com várias linhas se \\ slmult 1 a seguir. |
| \\ slmult *m*  | Segue o \\ SL. *m* = zero: pelo menos ou exatamente o espaçamento de linha, conforme descrito por \\ SL *n*. *m* = 1: espaçamento de linha = *n*/240 vezes com espaçamento de linha única.                                                                                                                              |
| \\ TB *n*      | Posição da guia da barra, em twips, da margem esquerda.                                                                                                                                                                                                                              |
| \\ tldot       | Pontos de preenchimento de tabulação.                                                                                                                                                                                                                                                               |
| \\ tleq        | Sinal de igual do preenchimento de guia.                                                                                                                                                                                                                                                         |
| \\ tlhyph      | Hifens de guia de tabulação.                                                                                                                                                                                                                                                            |
| \\ tlth        | Linha com preenchimento de guia espesso.                                                                                                                                                                                                                                                         |
| \\ tlul        | Preenchimento de guia sublinhado.                                                                                                                                                                                                                                                          |
| \\ tqc         | Guia centralizada.                                                                                                                                                                                                                                                                  |
| \\ tqdec       | Guia decimal.                                                                                                                                                                                                                                                                   |
| \\ tqr         | Guia de liberação para a direita.                                                                                                                                                                                                                                                               |
| \\ TX *n*      | Posição da guia, em twips, da margem esquerda.                                                                                                                                                                                                                                  |



 

**Palavras de controle de formato de caractere TOM RTF**

| Palavra de controle     | Significado                                                                                                                                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ animação *n* | Define o tipo de animação como *n*.                                                                                                                                                                                                              |
| \\ b             | Aplique.                                                                                                                                                                                                                                    |
| \\ capitula          | Todas as letras maiúsculas.                                                                                                                                                                                                                            |
| \\ CF *n*        | Cor do primeiro plano (o padrão é **tomAutocolor**).                                                                                                                                                                                      |
| \\ cs *n*        | Estilo de caractere *n*.                                                                                                                                                                                                                     |
| \\ DN *n*        | Posição do subscript em meio-ponto (o padrão é 6).                                                                                                                                                                                    |
| \\ embo          | Em alto-relevo.                                                                                                                                                                                                                                |
| \\ f *n*         | Número da fonte, *n* se refere a uma entrada na tabela de fontes.                                                                                                                                                                                   |
| \\*n* -FS        | Tamanho da fonte em meio-ponto (o padrão é 24).                                                                                                                                                                                            |
| \\ realçar *n* | Cor do plano de fundo (o padrão é **tomAutocolor**).                                                                                                                                                                                      |
| \\ Encontrei             | Colocadas.                                                                                                                                                                                                                                  |
| \\ impr          | Impressão.                                                                                                                                                                                                                                 |
| \\ lang *n*      | Aplica um idioma a um caractere. *n* é um número correspondente a um idioma. A \\ palavra de controle simples redefine a propriedade Language para o idioma definido por \\ deflang *n* nas propriedades do documento.                             |
| \\ nosupersub    | Desativa sobrescrito ou subscrito.                                                                                                                                                                                                      |
| \\ outl          | Descreve.                                                                                                                                                                                                                                 |
| \\ queixa         | Redefine as propriedades de formatação de caractere para um valor padrão definido pelo aplicativo. As propriedades de formatação de caractere associadas (descritas na seção Propriedades de caractere associadas na especificação de RTF) também são redefinidas. |
| \\ scaps         | Versalete.                                                                                                                                                                                                                          |
| \\ tonalidade          | Sombra.                                                                                                                                                                                                                                  |
| \\ posição        | Risca.                                                                                                                                                                                                                           |
| \\ projeto           | Aplica o subscrito ao texto e reduz o tamanho do ponto de acordo com as informações da fonte.                                                                                                                                                          |
| \\ tipo         | Aplica sobrescrito ao texto e reduz o tamanho do ponto de acordo com as informações da fonte.                                                                                                                                                        |
| \\ UL            | Sublinhado contínuo. \\ UL0 desativa todos os sublinhados.                                                                                                                                                                                  |
| \\ uld           | Sublinhado pontilhado.                                                                                                                                                                                                                        |
| \\ uldb          | Sublinhado duplo.                                                                                                                                                                                                                        |
| \\ ulnone        | Interrompe todos os sublinhados.                                                                                                                                                                                                                   |
| \\ ulw           | Palavra sublinhada.                                                                                                                                                                                                                          |
| \\ up *n*        | Posição de sobrescrito em meio-ponto (o padrão é 6).                                                                                                                                                                                  |
| \\ l             | Texto oculto.                                                                                                                                                                                                                             |



 

## <a name="finding-rich-text"></a>Localizando Rich Text

Você pode usar os métodos de TOM para localizar Rich Text, conforme definido por um intervalo de texto. Encontrar esse texto rico com precisão é necessário em processamento de texto, embora nunca tenha sido atendido em um processador de texto "o que você vê é o que você obtém" (WYSIWYG). Há claramente um domínio maior de correspondência de Rich Text que permite que algumas propriedades de formatação de caracteres sejam ignoradas (ou incluam formatação de parágrafo e/ou conteúdo de objeto), mas essas generalizações estão além do escopo desta seção.

Uma finalidade para essa funcionalidade é usar uma caixa de diálogo de **localização** de Rich Text para definir o Rich Text que você deseja localizar em um documento. A caixa de diálogo seria implementada usando um controle rich edit e os métodos TOM seriam usados para executar a pesquisa no documento. Você pode copiar o Rich Text desejado do documento para a caixa de diálogo **Localizar** ou inserir e formatá-lo diretamente na caixa de diálogo **Localizar** .

O exemplo a seguir mostra como usar os métodos de TOM para localizar texto contendo combinações de formatação de caractere exata. O algoritmo procura o texto sem formatação no intervalo de correspondência, que é nomeado `pr1` . Se o texto sem formatação for encontrado, ele será apontado por um intervalo de avaliação, denominado `pr2` . Em seguida, dois intervalos de ponto de inserção ( `prip1` e `prip2` ) são usados para percorrer o intervalo de avaliação comparando sua formatação de caractere com a do `pr1` . Se eles corresponderem exatamente, o intervalo de entrada (fornecido por `ppr` ) será atualizado para apontar para o texto do intervalo de avaliação e a função retornará a contagem de caracteres no intervalo correspondente. Dois objetos [**ITextFont**](/windows/desktop/api/Tom/nn-tom-itextfont) `pf1` e `pf2` são usados na comparação de formatação de caracteres. Eles são anexados aos intervalos de ponto de inserção `prip1` e `prip2` .


```
LONG FindRichText (
    ITextRange **ppr,             // Ptr to range to search
    ITextRange *pr1)              // Range with rich text to find
{
    BSTR        bstr;             // pr1 plain-text to search for
    LONG        cch;              // Text string count
    LONG        cch1, cch2;       // tomCharFormat run char counts
    LONG        cchMatch = 0;     // Nothing matched yet
    LONG        cp;               // Handy char position
    LONG        cpFirst1;         // pr1 cpFirst
    LONG        cpFirst2;         // pr2 cpFirst
    ITextFont  *    pf1, *pf      // Fonts corresponding to IPs prip1 and prip2
    ITextRange *pr2;              // Range duplicate to search with
    ITextRange *prip1, *prip      // Insertion points to walk pr1, pr2

    if (!ppr || !*ppr || !pr1)
        return E_INVALIDARG;

    // Initialize range and font objects used in search
    if ((*ppr)->GetDuplicate(&pr2)    != NOERROR ||
        pr1->GetDuplicate(&prip1)     != NOERROR ||
        pr2->GetDuplicate(&prip2)     != NOERROR ||
        prip1->GetFont(&pf1)          != NOERROR ||
        prip2->GetFont(&pf2)          != NOERROR ||
        pr1->GetText(&bstr)           != NOERROR )
    {
        return E_OUTOFMEMORY;
    }

    pr1->GetStart(&cpFirst1);

    // Keep searching till rich text is matched or no more plain-text hits
    while(!cchMatch && pr2->FindText(bstr, tomForward, 0, &cch) == NOERROR)
    {
        pr2->GetStart(&cpFirst2);                 // pr2 is a new trial range
        prip1->SetRange(cpFirst1, cpFirst1);      // Set up IPs to scan match
        prip2->SetRange(cpFirst2, cpFirst2);      //  and trial ranges

        while(cch > 0 &&
            pf1->IsEqual(pf2, NULL) == NOERROR)   // Walk match & trial ranges
        {                                         //  together comparing font
            prip1->GetStart(&cch1);               //  properties
            prip1->Move(tomCharFormat, 1, NULL);
            prip1->GetStart(&cp);
            cch1 = cp - cch1;                     // cch of next match font run

            prip2->GetStart(&cch2);
            prip2->Move(tomCharFormat, 1, NULL);
            prip2->GetStart(&cp);
            cch2 = cp - cch2;                      // cch of next trial font run

            if(cch1 < cch)                         // There is more to compare
            {
                if(cch1 != cch2)                   // Different run lengths:
                    break;                         //  no formatting match
                cch = cch - cch1;                  // Matched format run
            }
            else if(cch2 < cch)                    // Trial range format run too
                break;                             //  short

            else                                   // Both match and trial runs
            {                                      //  reach at least to match
                pr2->GetEnd(&cp);                  //  text end: rich-text match
                (*ppr)->SetRange(cpFirst2, cp)     // Set input range to hit
                cchMatch = cp - cpFirst2;          //  coordinates and return
                break;                             //  length of matched string
            }
        }
    }
    pr2->Release();
    prip1->Release();
    prip2->Release();
    pf1->Release();
    pf2->Release();
    SysFreeString(bstr);

    return cchMatch;
}
```



## <a name="tom-accessibility"></a>TOM de acessibilidade

José fornece suporte de acessibilidade por meio das interfaces [**ITextSelection**](/windows/desktop/api/Tom/nn-tom-itextselection) e [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) . Esta seção descreve os métodos que são úteis para acessibilidade e como um programa pode determinar a posição *x*, *y* da tela de um objeto.

Como os programas de acessibilidade baseados em interface do usuário normalmente funcionam com a tela e com o mouse, uma preocupação comum é encontrar a interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) correspondente para o local atual do mouse (em coordenadas de tela). As seções a seguir apresentam duas maneiras de determinar a interface correta:

-   [Por meio da tabela de objeto em execução](#interface-from-running-object-table)
-   Por meio da mensagem em [**\_ GETOLEINTERFACE**](em-getoleinterface.md) , que funciona para instâncias de edição ricas em janelas, desde que o cliente esteja no mesmo espaço de processo (não é necessário *realizar marshaling* )

Para obter mais informações, consulte a especificação de Acessibilidade Ativa da Microsoft. Depois de obter um objeto de uma posição de tela, você pode usar para uma interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) e chamar o método [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) para obter um objeto Range vazio na CP correspondente à posição da tela.

### <a name="interface-from-running-object-table"></a>Interface da tabela de objetos em execução

Uma corrompidos (tabela de objetos em execução) informa quais instâncias de objeto estão ativas. Ao consultar essa tabela, você pode acelerar o processo de conexão de um cliente com um objeto quando o objeto já estiver em execução. Antes que os programas possam acessar José interfaces por meio da tabela de objetos em execução, uma instância de TOM com uma janela precisa ser registrada no corrompidos usando um moniker. Você constrói o moniker a partir de uma cadeia de caracteres que contém o valor hexadecimal de seu [**HWND**](/windows/desktop/WinProg/windows-data-types). O exemplo de código a seguir mostra como fazer isso.


```
// This TOM implementation code is executed when a new windowed 
// instance starts up. 
// Variables with leading underscores are members of this class.

HRESULT hr;
OLECHAR szBuf[10];            // Place to put moniker
MONIKER *pmk;

hr = StringCchPrintf(szBuff, 10, "%x", _hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
OleStdRegisterAsRunning(this, pmk, &_dwROTcookie);
....................
 
// Accessibility Client: 
//    Find hwnd for window pointed to by mouse cursor.

GetCursorPos(&pt);
hwnd = WindowFromPoint(pt);

// Look in ROT (running object table) for an object attached to hwnd

hr = StringCchPrintf(szBuff, 10, "%x", hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
CreateBindContext(0, &pbc);
pmk->BindToObject(pbc, NULL, IID_ITextDocument, &pDoc);
pbc->Release();

if( pDoc )
{
    pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
    // ...now do whatever with the range pRange
}
```



### <a name="interface-from-window-messages"></a>Interface de mensagens de janela

A mensagem em [**\_ GETOLEINTERFACE**](em-getoleinterface.md) fornece outra maneira de obter uma interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para um objeto em uma determinada posição de tela. Conforme descrito em [interface na tabela de objetos em execução](#interface-from-running-object-table), você obtém um [**HWND**](/windows/desktop/WinProg/windows-data-types) para a posição da tela e, em seguida, envia essa mensagem para o **hWnd**. A mensagem em **\_ GETOLEINTERFACE** é específica de edição avançada e retorna um ponteiro para uma interface [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) na variável endereçada por *lParam*.

**Dica** Se um ponteiro for retornado (certifique-se de definir o objeto para o qual o *lParam* aponta para NULL antes de enviar a mensagem), você pode chamar seu método [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter uma interface [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) . O exemplo de código a seguir ilustra essa abordagem.


```
    HWND    hwnd;
    ITextDocument *pDoc;
    ITextRange *pRange;
    POINT    pt;
    IUnknown *pUnk = NULL;
    
    GetCursorPos(&pt);
    hwnd = WindowFromPoint(pt);
    SendMessage(hwnd, EM_GETOLEINTERFACE, 0, (LPARAM)&pUnk);
    if(pUnk && 
        pUnk->QueryInterface(IID_ITextDocument, &pDoc) == NOERROR)
    {
        pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
        //  ... continue with rest of program
    }
```



### <a name="accessibility-oriented-methods"></a>Métodos orientados a acessibilidade

Alguns métodos TOM são particularmente úteis para navegar pela tela, enquanto outros José métodos aprimoram o que você pode fazer quando chega a locais de interesse. A tabela a seguir descreve os métodos mais úteis.



| Método                                                 | Como a ti promove a acessibilidade                                                                                                                                                                 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getseleções**](/windows/desktop/api/Tom/nf-tom-itextdocument-getselection)     | Esse método obtém a seleção ativa que pode ser usada para uma variedade de finalidades orientadas por exibição, como realçar texto e rolagem.                                                      |
| [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) | Quando usado em uma seleção ativa, esse método tem a garantia de obter um intervalo associado a uma exibição específica.                                                                                 |
| [**Expanda**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)                    | Amplia um intervalo de texto para que todas as unidades parciais que ele contém estejam completamente contidas. Por exemplo, `Expand(tomWindow)` expande o intervalo para incluir a parte visível da história do intervalo. |
| [**Getduplicar**](/windows/desktop/api/Tom/nf-tom-itextrange-getduplicate)        | Quando usado em uma seleção ativa, esse método tem a garantia de obter um intervalo associado a uma exibição específica. Consulte a descrição de [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint).  |
| [**GetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-getpoint)                | Obtém as coordenadas da tela para a posição do caractere inicial ou final no intervalo de texto.                                                                                                        |
| [**ScrollIntoView**](/windows/desktop/api/Tom/nf-tom-itextrange-scrollintoview)    | Rola um intervalo de texto para a exibição.                                                                                                                                                               |
| [**Irá**](/windows/desktop/api/Tom/nf-tom-itextrange-setpoint)                | Seleciona o texto em um ponto especificado.                                                                                                                                              |



 

## <a name="character-match-sets"></a>Conjuntos de correspondência de caracteres

O parâmetro *Variant* dos vários métodos **move** \* em [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange), como [**MoveWhile**](/windows/desktop/api/Tom/nf-tom-itextrange-movewhile) e [**MoveUntil**](/windows/desktop/api/Tom/nf-tom-itextrange-moveuntil), pode usar uma cadeia de caracteres explícita ou um índice de 32 bits de conjunto de correspondência de caracteres. Os índices são definidos por intervalos Unicode ou conjuntos de caracteres [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) . O intervalo Unicode a partir de *n* e de comprimento *l* (< 32768) é fornecido pelo índice *n* + (*l <*< 16) + 0x80000000. Por exemplo, as letras gregas básicas são definidas por CR \_ grego = 0x805f0370 e os caracteres ASCII imprimíveis são definidos por CR \_ ASCIIPrint = 0x805e0020. Além disso, os métodos **MoveWhile** e **MoveUntil** permitem que você ignore rapidamente um intervalo de caracteres em qualquer conjunto de caracteres **GetStringTypeEx** ou em um intervalo de caracteres que não esteja em um desses conjuntos de caracteres.

Os conjuntos de [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) são especificados pelos valores para *Ctype1*, *Ctype2* e *Ctype3*, e são definidos da seguinte maneira.



| Cset                 | Significado                          |
|----------------------|----------------------------------|
| *Ctype1*             | Combinação de \_ tipos CTYPE1 CT. |
| *Ctype2* + tomCType2 | Qualquer \_ tipo de CTYPE2 CT.             |
| *Ctype3* + tomCType3 | Combinação de \_ tipos CTYPE3 CT. |



 

Especificamente, o *Ctype1* pode ser qualquer combinação do seguinte.



| Nome do Ctype1 | Valor  | Significado                                                           |
|-------------|--------|-------------------------------------------------------------------|
| \_Superior C1   | 0x0001 | Letras maiúsculas.                                                        |
| \_Parte inferior C1   | 0x0002 | Minúsculas.                                                        |
| \_Dígito C1   | 0x0004 | Dígitos decimais.                                                   |
| \_Espaço C1   | 0x0008 | Caracteres de espaço.                                                 |
| \_PUNCT C1   | 0x0010 | Pontuação.                                                      |
| \_Tab C1   | 0x0020 | Caracteres de controle.                                               |
| C1 \_ em branco   | 0x0040 | Caracteres em branco.                                                 |
| \_XDIGIT C1  | 0x0080 | Dígitos hexadecimais.                                               |
| \_Alfa C1   | 0x0100 | Qualquer caractere linguístico (alphabetic, syllabary ou ideográfica). |
| C1 \_ definido | 0x0200 | Um caractere definido, mas não um dos outros tipos C1 \_ \* .       |



 

Os tipos *Ctype2* dão suporte ao layout adequado de texto Unicode. Os atributos de direção são atribuídos para que o algoritmo de layout bidirecional padronizado por Unicode produza resultados precisos. Esses tipos são mutuamente exclusivos. Para obter mais informações sobre o uso desses atributos, consulte *o padrão Unicode: codificação de caracteres mundiais, volumes 1 e 2*, Addison-Wesley empresa de publicação: 1991, 1992.



| Nome do CType2          | Valor | Significado                          |
|----------------------|-------|----------------------------------|
| Tipa              |       |                                  |
| \_LEFTTORIGHT C2      | 0x1   | Da esquerda para a direita.                   |
| RIGHTTOLEFT de C2 \_      | 0x2   | Da direita para a esquerda.                   |
| Baixas                |       |                                  |
| \_EUROPENUMBER C2     | 0x3   | Número Europeu, dígito Europeu. |
| \_EUROPESEPARATOR C2  | 0x4   | Separador numérico Europeu.      |
| \_EUROPETERMINATOR C2 | 0x5   | Terminador numérico Europeu.     |
| \_ARABICNUMBER C2     | 0x6   | Número árabe.                   |
| \_COMMONSEPARATOR C2  | 0x7   | Separador numérico comum.        |
| Neutro             |       |                                  |
| \_BLOCKSEPARATOR C2   | 0x8   | Separador de bloco.                 |
| \_SEGMENTSEPARATOR C2 | 0x9   | Separador de segmento.               |
| \_Espaço em branco C2       | 0xA   | Espaço em branco.                     |
| \_OTHERNEUTRAL C2     | 0xB   | Outros neutros.                  |
| Não aplicável:      |       |                                  |
| C2 não \_ aplicável    | 0x0   | Sem direção implícita.           |



 

Os tipos *Ctype3* devem ser espaços reservados para extensões para os tipos POSIX necessários para o processamento de texto geral ou para as funções de biblioteca C padrão.



| Nome do CType3       | Valor  | Significado                                                             |
|-------------------|--------|---------------------------------------------------------------------|
| Não \_ espaçamento C3    | 0x1    | Marca de não espaçamento.                                                    |
| \_Diacríticos C3     | 0x2    | Marca de não espaçamento diacrítico.                                          |
| \_VOWELMARK C3     | 0x4    | Marca de não espaçamento de vogal.                                              |
| \_Símbolo C3        | 0x8    | Símbolo.                                                             |
| \_Katakana C3      | 0x10   | Caractere katakana.                                                 |
| C3 \_ Hiragana      | 0x20   | Caractere hiragana.                                                 |
| \_Largura C3     | 0x40   | Caractere de meia largura.                                               |
| \_Largura total C3     | 0x80   | Caractere de largura inteira.                                               |
| \_Ideograma de C3     | 0x100  | Caractere ideográfica.                                              |
| \_Kashida do C3       | 0x200  | Caractere de kashida em árabe.                                           |
| \_Alfa C3         | 0x8000 | Todos os caracteres lingüísticos (alphabetic, syllabary e ideográfica). |
| C3 não \_ aplicável | 0x0    | Não aplicável.                                                     |



 

Um EDK (Kit de desenvolvimento de edição) pode incluir definições de índice *pvar* para os seguintes intervalos descritos no padrão Unicode.



| Conjunto de caracteres         | Intervalo Unicode | Conjunto de caracteres             | Intervalo Unicode |
|-----------------------|---------------|---------------------------|---------------|
| ASCII                 | 0x0 – 0x7F      | ANSI                      | 0x0 – 0xFF      |
| ASCIIPrint            | 0x20 – 0x7E     | Latino1                    | 0x20 – 0xFF     |
| Latin1Supp            | 0XA0 – 0xFF     | LatinXA                   | 0x100—0x17f   |
| LatinXB               | 0x180—0x24f   | IPAX                      | 0x250—0x2af   |
| SpaceMod              | 0x2b0—0x2ff   | Trema                 | 0x300—0x36f   |
| Grego                 | 0x370—0x3ff   | BasicGreek                | 0x370—0x3cf   |
| GreekSymbols          | 0x3d0—0x3ff   | Cirílico                  | 0x400—0x4ff   |
| Armênia              | 0x530—0x58f   | Hebraico                    | 0x590—0x5ff   |
| BasicHebrew           | 0x5d0—0x5ea   | HebrewXA                  | 0x590—0x5cf   |
| HebrewXB              | 0x5eb—0x5ff   | Árabe                    | 0x600—0x6ff   |
| BasicArabic           | 0x600—0x652   | ArabicX                   | 0x653—0x6ff   |
| Devangari             | 0x900—0x97f   | Bengali (anteriormente Bengali) | 0x980—0x9ff   |
| Gurmukhi              | 0xa00—0xa7f   | Guzerate                  | 0xa80—0xaff   |
| Odia (anteriormente, odia) | 0xb00—0xb7f   | Tâmil                     | 0xb80—0xbff   |
| Teluga                | 0xc00—0xc7f   | canarim                   | 0xc80—0xcff   |
| Malaiala             | 0xd00—0xd7f   | Tailandês                      | 0xe00—0xe7f   |
| Lao                   | 0xe80—0xeff   | GeorgianX                 | 0x10a0—0xa0cf |
| BascGeorgian          | 0x10d0—0x10ff | Jamo                      | 0x1100—0x11ff |
| LatinXAdd             | 0x1e00—0x1eff | GreekX                    | 0x1f00—0x1fff |
| GenPunct              | 0x2000—0x206f | Sobrescrito               | 0x2070—0x207f |
| Subscrito             | 0x2080—0x208f | SuperSubscript            | 0x2070—0x209f |
| Moeda              | 0x20a0—0x20cf | CombMarkSym               | 0x20d0—0x20ff |
| LetterLike            | 0x2100—0x214f | NumberForms               | 0x2150—0x218f |
| Setas                | 0x2190—0x21ff | MathOps                   | 0x2200—0x22ff |
| MiscTech              | 0x2300—0x23ff | CtrlPictures              | 0x2400—0x243f |
| OptCharRecog          | 0x2440—0x245f | EnclAlphaNum              | 0x2460—x24ff  |
| BoxDrawing            | 0x2500—0x257f | Blocoelement              | 0x2580—0x259f |
| GeometShapes          | 0x25a0—0x25ff | MiscSymbols               | 0x2600—0x26ff |
| Dingbats              | 0x2700—0x27bf | CJKSymPunct               | 0x3000—0x303f |
| Hiragana              | 0x3040—0x309f | Katakana                  | 0x30a0—0x30ff |
| Bopomofo              | 0x3100—0x312f | HangulJamo                | 0x3130—0x318f |
| CJLMisc               | 0x3190—0x319f | EnclCJK                   | 0x3200—0x32ff |
| CJKCompatibl          | 0x3300—0x33ff | Han                       | 0x3400—0xabff |
| Hangul                | 0xac00—0xd7ff | UTF16Lead                 | 0xD800 – 0xDBFF |
| UTF16Trail            | 0xDC00 – 0xDFFF | PrivateUse                | 0xe000—0xf800 |
| CJKCompIdeog          | 0xf900—0xfaff | AlphaPres                 | 0xfb00—0xfb4f |
| ArabicPresA           | 0xfb50—0xfdff | CombHalfMark              | 0xfe20—0xfe2f |
| CJKCompForm           | 0xfe30—0xfe4f | SmallFormVar              | 0xfe50—0xfe6f |
| ArabicPresB           | 0xfe70—0xfefe | HalfFullForm              | 0xff00—0xffef |
| Especialidades              | 0xfff0—0xfffd |                           |               |



 

 

 