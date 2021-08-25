---
description: O Painel de Entrada do Computador Tablet da Microsoft é uma ferramenta poderosa para inserir texto manuscrito com uma caneta e corrigir texto sem o uso de um teclado.
ms.assetid: c45ac1b5-7713-4bcb-a130-4692cff99aa2
title: Habilitando a correção de texto para coletores de tinta personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accb0bf2129a4e93e543e3ec5cc73d3e65383dc57b581114f30e812b1ac88b8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940817"
---
# <a name="enabling-text-correction-for-custom-ink-collectors"></a>Habilitando a correção de texto para coletores de tinta personalizados

O Painel de Entrada do Computador Tablet da Microsoft é uma ferramenta poderosa para inserir texto manuscrito com uma caneta e corrigir texto sem o uso de um teclado. Ao usar o Painel de Entrada, um usuário ins muita atenção ao digitar texto nas superfícies de escrita do Painel de Entrada, o que faz com que o Painel de Entrada reconheça o manuscrito do usuário como texto. Depois que o texto tiver sido reconhecido, o usuário tocará em Inserir no Painel de Entrada para inserir o texto em um aplicativo ou documento. Antes de inserir o texto, um usuário tem acesso a um conjunto de ferramentas de correção no Painel de Entrada. Isso inclui a seleção de um resultado de reconhecimento alternativo, a capacidade de reescrever um único caractere ou até mesmo a reescrita de toda a palavra. Essas ferramentas de correção permitem que um usuário corrija erros de reconhecimento e de humanos.

Depois que o texto inserido usando o Painel de Entrada está no documento, os usuários têm acesso à mesma funcionalidade de correção que está disponível antes da inserção em aplicativos baseados em [Windows Estrutura de Serviços de Texto](/windows/desktop/TSF/text-services-framework)e habilitados para Serviços de Texto. A partir do Microsoft Windows XP Service Pack 2 Tablet PC Edition, todos os aplicativos rich edit são habilitados por padrão para Serviços de Texto e, a partir do Windows Vista, os aplicativos HTML são habilitados para Serviços de Texto por padrão. A correção no documento só está disponível em aplicativos habilitados e baseados no Serviço de Texto; isso porque o Painel de Entrada depende da capacidade do Serviço de Texto de armazenar propriedades de texto associadas, incluindo objetos de tinta e alternativas de reconhecimento, para fornecer correção no documento.

![painel de entrada do tablet pc com correção de texto](images/a0dced5e-16de-410b-965f-5d97d297cee5.jpg)

No entanto, há vários cenários, incluindo a correção do reconhecimento de fala ou a correção de texto digitado em qualquer lugar, que não começam com a entrada de texto usando o Painel de Entrada, mas no qual a correção no documento pode ser extremamente útil para usuários de tablet pc. Um exemplo principal está em aplicativos que fornecem superfícies de tinta personalizadas para inserir texto usando uma caneta. As superfícies de mascaramento personalizadas são uma ótima maneira de os aplicativos fornecerem funcionalidades personalizadas exclusivamente específicas para as tarefas de entrada de texto de cada aplicativo. Além disso, as superfícies de tinta personalizadas fornecem uma experiência de usuário totalmente integrada do Tablet PC, o que deixa claro que a caneta é um dispositivo de entrada de primeira classe em aplicativos que os contêm. No entanto, os aplicativos que fornecem superfícies de mascaramento personalizadas podem não permitir ou não podem fornecer o mesmo nível de suporte de correção que está disponível no Painel de Entrada na correção do documento.

![coletor de tinta personalizado](images/b6797b12-dda6-44c4-87f4-570fe0c23f3a.jpg)

Os Serviços de Texto baseados ou habilitados em aplicativos nos quais a correção no documento é útil para correção de texto não inserido usando o Painel de Entrada são capazes de usar a API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) do Painel de Entrada ([classe Microsoft.TextInput.HandwrittenTextInsertion](/previous-versions/ms573516(v=vs.100)) no código gerenciado) para habilitar a correção no documento para texto inserido por outros meios. Dessa forma, os aplicativos podem adicionar um suporte de correção eficiente às superfícies de mascaramento personalizadas ou a outros cenários de entrada de texto e arredondar a história de entrada de texto do tablet pc. A API IHandWrittenTextInsertion do painel de entrada é incluída como parte do sistema operacional Windows Vista e como parte do SDK da Plataforma de Tablet versão 1.9 ou mais recente. Uma versão baseada em .NET e COM da API está incluída. A habilitação da correção no documento para texto não inserido usando o Painel de Entrada tem suporte Windows Vista e mais novos. A correção no documento só está disponível para idiomas latinos e não pode exibir nenhum caractere fora do conjunto de caracteres latinos.

## <a name="how-to-use-the-handwrittentextinsertion-api-in-an-application"></a>Como usar a API HandwrittenTextInsertion em um aplicativo

As alterações necessárias em um aplicativo para integrar a correção do Painel de Entrada no documento para texto não inserido usando o Painel de Entrada e usando a API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) são simples. Todo o código de entrada de texto personalizado do aplicativo permanece inalterado, exceto para a última etapa. No ponto em que o texto inserido usando uma superfície de escrita personalizada, o reconhecimento de fala ou outros meios deve ser exibido em um campo de texto habilitado para serviços de texto, o aplicativo envia o texto para a interface **IHandWrittenTextInsertion** em vez de enviá-lo diretamente para o campo de texto. Em seguida, o componente de programação do Painel de Entrada lida com a inserção do texto no campo de texto e no armazenamento de back-back dos Serviços de Texto. Ao adicionar o texto ao armazenamento de back-back dos Serviços de Texto, o componente de programação do Painel de Entrada lida com a configuração das propriedades de texto exigidas pelo Painel de Entrada para que a correção no documento seja habilitada para esse texto.

A seção a seguir explica esse processo em detalhes para um aplicativo C++ usando a versão COM da API [**IHandWrittenTextInsertion.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) Há observações em qualquer lugar em que as etapas para usar .NET Framework versão da API em C diferem para a versão \# com using no C++. A API **HandwrittenTextInsertion gerenciada** inclui uma única interface COM, **IHandwrittenTextInsertion.** A definição dessa interface está localizada em PenInputPanel.h e PenInputPanel \_ i.c.

Primeiro, o aplicativo deve usar a [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para produzir uma instância [**de IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) com a id da classe **CLSID \_ HandwrittenTextInsertion**. Observe que a criação de um objeto **\_ HandwrittenTextInsertion CLSID** terá êxito somente depois que uma janela for criada e receber o foco, porque até lá, o armazenamento de back-back dos Serviços de Texto não será ativado. Além disso, se tiptsf.dll estiver presente no sistema, a função **CoCreateInstance** falhará e retornará **REGDB \_ E \_ CLASSNOTREG**, indicando que a correção no documento do Painel de Entrada não tem suporte no sistema. Neste ponto, o aplicativo deve continuar sem tentar habilitar a correção do Painel de Entrada no documento. A instância de **HandwrittenTextInsertion** deve ser acessível do código do aplicativo que lida com a inserção de texto em um campo de texto.

> [!Note]  
> Ao trabalhar com a .NET Framework da API, o aplicativo deve adicionar uma instrução using para permitir o acesso ao namespace [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) e, em seguida, criar o objeto diretamente.

 

Em segundo lugar, o código do aplicativo que é responsável por inserir texto em um campo de texto deve ser alterado para que ele não insere mais texto em um campo de texto diretamente, mas chama um ou outro dos dois métodos de inserção de [**IHandwrittenTextInsertion.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) Se os aplicativos devem optar por chamar [**InsertRecognitionResultsArray**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray) ou [**InsertRecognitionResults**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult) depende se o aplicativo tem as alternativas de reconhecimento para o texto armazenado como uma matriz ou como um objeto [**IInkRecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)

> [!Note]  
> Ao trabalhar em código gerenciado, o objeto de reconhecimento correspondente consumido por InsertRecognitionResultsArray é [RecognitionResult.](/previous-versions/ms552537(v=vs.100)) Ambos os métodos consomem os três parâmetros a seguir:

 

-   *alternativas* É uma coleção bidimensional de cadeias de caracteres, armazenada como uma matriz de matrizes ou como um [**objeto IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) (ou [RecognitionResult](/previous-versions/ms552537(v=vs.100))). Se as alternativas são armazenadas como uma matriz de matrizes, ela deve ser passada como um ponteiro de matriz segura. Cada entrada na matriz de nível superior é uma lista de alternativas para uma única palavra na inserção. A entrada na posição zero nas sub-matrizes de alternativas é o texto inserido no campo de texto. As alternativas adicionais (índices 1 a n em cada sub-matriz) são armazenadas no armazenamento de backing dos Serviços de Texto e oferecidas ao usuário como opções como parte da correção no documento. Se as alternativas não são incluídas, o usuário vê 'Sem sugestão' no lugar da lista de alternativas. Se uma inserção contiver várias palavras com espaços entre elas, cada espaço deverá ser incluído como uma entrada na matriz de nível superior.
-   *idioma* O [LCID de Linguagem de](/previous-versions/ms221397(v=vs.71)) Entrada que corresponde ao texto contido no *parâmetro alternates.* No caso em que  o conteúdo das alternativas foi gerado por um manuscrito ou reconhecedor de fala, essa também é a propriedade [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) associada ao reconhecedor usado.
-   *fLatticeContainsAutoSpacingInformation* Um sinalizador que indica se o texto contido no parâmetro *alternates* foi gerado por um reconhecedor com espaçamento automático habilitado. Se o espaçamento automático tiver sido habilitado, o sinalizador deverá ser definido como **TRUE.** Se o espaçamento automático tiver sido desabilitado, o sinalizador deverá ser definido como **FALSE.** No caso em que  o conteúdo das alternativas foi gerado por um reconhecedor que não dá suporte ao espaçamento automático ou não foi gerado por um reconhecedor, o sinalizador deve ser definido como **FALSE.**

O modelo de programação do Painel de Entrada é capaz de inserir o texto no documento ou aplicativo da posição do cursor do sistema.

Ambos os métodos retornarão **S \_ OK** se a inserção for bem-sucedida. Eles **retornarão E \_ NOINTERFACE** se o aplicativo não for baseado em Serviços de Texto ou habilitado e **E \_ INVALIDARG** se as alternativas estão formatadas incorretamente ou inacessíveis.  Eles também poderão retornar **E \_ OUTOFMEMORY** se não houver memória suficiente disponível no sistema ou **E \_ FAIL** após uma falha catastrófica, como a Estrutura de Serviços de Texto não está habilitada.

### <a name="conclusion"></a>Conclusão

Habilitar a correção no documento do Painel de Entrada para texto não inserido usando o Painel de Entrada é uma maneira barata e fácil para um aplicativo baseado em Serviços de Texto ou habilitado complementar um método de entrada ou de tinta personalizado com funcionalidade avançada de correção baseada em caneta. No Windows Vista, todos os aplicativos Rich Edit e Trident são Serviços de Texto habilitados. Embora as superfícies de mascaramento integradas sejam uma ótima opção para adicionar uma experiência de usuário personalizada do Tablet PC a um aplicativo, elas só darão suporte à metade da entrada de texto se não incluíram recursos de correção. A correção no documento fornece aos usuários a outra metade da história adicionando a capacidade de trocar uma seleção por uma alternativa de reconhecimento ou reescrever parte ou toda a seleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Programando o painel de entrada de texto](programming-the-text-input-panel.md)
</dt> </dl>

 

 
