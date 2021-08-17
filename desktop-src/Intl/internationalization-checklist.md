---
description: Este tópico fornece ações a serem executadas para criar um código que dê suporte a vários mercados. Considere essas instruções como um guia durante o design do código e as métricas ao avaliar as compilações.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Lista de verificação de internacionalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4650f7bd1111f35c911d6efe12bfbec4b537f2cdabdc50160965b5e602708b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147509"
---
# <a name="internationalization-checklist"></a>Lista de verificação de internacionalização

Este tópico fornece ações a serem executadas para criar um código que dê suporte a vários mercados. Considere essas instruções como um guia durante o design do código e as métricas ao avaliar as compilações.

-   Crie especificações de programa que contam para considerações internacionais desde o início.
    -   Crie ícones e bitmaps para serem significativos e não ofensivos em seus mercados de destino e não contenham texto.
    -   Menus de design e caixas de diálogo para deixar espaço para a expansão de texto. Por exemplo, cadeias de caracteres em inglês geralmente se expandem por 40% quando convertidas em alemão ou holandês.
    -   Não use referências gírias ou culturalmente específicas em mensagens ou elementos de interface do usuário.
    -   Crie combinações de teclas de atalho que são acessíveis em teclados internacionais. Por exemplo, evite usar chaves de caractere de Pontuação como teclas de atalho porque elas nem sempre são encontradas em teclados internacionais ou facilmente produzidas pelo usuário. para obter exemplos de layouts de teclado, consulte [Windows layouts de teclado](https://msdn.microsoft.com/goglobal/bb964651.aspx).
    -   Considere as leis locais que afetam os designs de recursos, como requisitos que as entidades governamentais adquirem software que dá suporte a vários idiomas oficiais.
    -   Desenvolva contratos de terceiros que dão suporte aos padrões da interface do usuário internacional da sua organização e às decisões de design.
    -   Use uma terminologia consistente nas cadeias de caracteres da interface do usuário que devem ser convertidas.

<!-- -->

-   Crie um código que seja independente da localidade.
    -   Não concatene cadeias de caracteres para formar frases.
    -   Não use uma determinada variável de cadeia de caracteres em mais de um contexto, como reutilizar um fragmento de frase em mensagens e prompts diferentes, pois essas cadeias de caracteres podem não ser facilmente traduzidas.
    -   Documente cadeias de caracteres usando comentários para fornecer contexto para tradutores e marque claramente as cadeias de caracteres ou os personagens que não devem ser localizados.
    -   Não use constantes de caractere embutido em código, constantes numéricas, posições de tela, nomes de filenames ou demarcadores que presumim um idioma específico.
    -   Torne os buffers grandes o suficiente para manter as cadeias de caracteres traduzidas.
    -   Permitir a entrada de dados com formatos que variam por localidade, como datas, horas e moedas.
    -   Use o tamanho do papel, o tamanho do envelope e outros padrões apropriados para uma determinada localidade.
    -   Certifique-se de que cada edição de idioma possa ler documentos criados pelas outras edições.
    -   Forneça suporte para hardware específico de localidade, se necessário.
    -   Configure recursos que não se aplicam a mercados internacionais como opções de implementação que podem ser desativadas facilmente.

<!-- -->

-   Crie código que aproveita a funcionalidade internacional oferecida pelo Microsoft Windows.
    -   Use informações internacionais transportadas pelo sistema (suporte ao idioma nacional).
    -   Use funções do sistema para classificação, conversão de casos e mapeamento de cadeia de caracteres.
    -   Use funções de layout de texto genérico.
    -   Responda a alterações nas configurações internacionais no painel de controle.
    -   Manipule a mensagem do WM \_ INPUTLANGCHANGEREQUEST.
    -   Suporte a editores de método de entrada, texto vertical e regras de quebra de linha nas edições do leste asiático.

<!-- -->

-   Compile todas as edições internacionais do programa de um conjunto de arquivos de origem.
    -   Minimize ou elimine os mecanismos que exigem que o código seja recompilado para diferentes edições de idioma.
    -   armazene itens localizáveis, como cadeias de caracteres e ícones, em Windows arquivos de recursos.
    -   Armazene documentos em todas as edições de idioma usando o mesmo formato de arquivo.

<!-- -->

-   Dão suporte a conjuntos de caracteres diferentes, não apenas à página de código latino 1, número 1252.
    -   O programa dá suporte a ambientes de rede nos quais os computadores executam sistemas operacionais com páginas de código padrão diferentes.
    -   Use GetCPInfoEx para recuperar intervalos de bytes potenciais para páginas de código do leste asiático.
    -   Analisar caracteres de byte duplo no leste asiático – aplicativos de idioma, a menos que o código seja baseado em Unicode.
    -   Suporte a Unicode ou conversão entre Unicode e a página de código local.
    -   Não presuma que todos os caracteres sejam de 8 bits ou de 16 bits.
    -   Use tipos de dados genéricos e protótipos de função genéricos.
    -   Use a propriedade charset de fonte, que chama EnumFontFamiliesEx e a função de caixa de diálogo comum ChooseFont.
    -   Exiba e imprima o texto usando as fontes apropriadas para a localidade.

<!-- -->

-   Teste os recursos internacionais do programa.
    -   O texto traduzido deve atender aos padrões de oradores nativos.
    -   As caixas de diálogo devem ser redimensionadas corretamente e o texto deve ser hifenizado adequadamente, quando idiomas diferentes são exibidos.
    -   Caixas de diálogo, barras de status, barras de ferramentas e menus devem caber na tela e ler legibly quando a exibição é definida em resoluções diferentes, para todos os idiomas traduzidos.
    -   Os aceleradores de menu e caixa de diálogo devem ser exclusivos.
    -   Os usuários devem ser capazes de digitar caracteres de scripts não europeus em documentos, caixas de diálogo e nomes de texto.
    -   Os usuários devem ser capazes de recortar, colar, salvar e imprimir caracteres de scripts não europeus com êxito.
    -   A classificação e a conversão de casos devem ser precisas para localidades diferentes.
    -   O aplicativo deve funcionar corretamente em edições localizadas do Windows.

 

 



