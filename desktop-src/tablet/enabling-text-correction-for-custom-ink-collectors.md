---
description: O painel de entrada do Microsoft Tablet PC é uma ferramenta poderosa para inserir texto manuscrito com uma caneta e corrigir o texto sem o uso de um teclado.
ms.assetid: c45ac1b5-7713-4bcb-a130-4692cff99aa2
title: Habilitando a correção de texto para coletores de tinta personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4dee4c7dfee1489cd002848c496be41f73d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553946"
---
# <a name="enabling-text-correction-for-custom-ink-collectors"></a>Habilitando a correção de texto para coletores de tinta personalizados

O painel de entrada do Microsoft Tablet PC é uma ferramenta poderosa para inserir texto manuscrito com uma caneta e corrigir o texto sem o uso de um teclado. Ao usar o painel de entrada, um usuário insere o texto manuscrito nas superfícies de tinta do painel de entrada, o que faz com que o painel de entrada reconheça o manuscrito do usuário como texto. Depois que o texto for reconhecido, o usuário toca em inserir no painel de entrada para inserir o texto em um aplicativo ou documento. Antes de inserir o texto, um usuário tem acesso a um conjunto de ferramentas de correção no painel de entrada. Isso inclui a seleção de um resultado de reconhecimento alternativo, a capacidade de reescrever um único caractere ou até mesmo para riscar toda a palavra e reescrever. Essas ferramentas de correção permitem que um usuário corrija erros de reconhecimento e erros humanos.

Depois que o texto inserido usando o painel de entrada estiver no documento, os usuários terão acesso à mesma funcionalidade de correção que está disponível antes da inserção nos aplicativos baseados em [estrutura de serviços de texto](/windows/desktop/TSF/text-services-framework)do Windows e habilitados para serviços de texto. A partir do Microsoft Windows XP Service Pack 2 Tablet PC Edition, todos os aplicativos de edição avançados são habilitados para serviços de texto por padrão e, a partir do Windows Vista, os aplicativos HTML são habilitados para serviços de texto por padrão. A correção no documento só está disponível em aplicativos baseados em serviço de texto e habilitados; Isso ocorre porque o painel de entrada depende da capacidade do serviço de texto de armazenar propriedades de texto associadas, incluindo objetos de tinta e alternativas de reconhecimento, a fim de fornecer a correção no documento.

![painel de entrada do Tablet PC com correção de texto](images/a0dced5e-16de-410b-965f-5d97d297cee5.jpg)

No entanto, há inúmeros cenários, incluindo correção de reconhecimento de fala ou correção de texto digitado no Go, que não começam com entrada de texto usando o painel de entrada, mas em que a correção no documento pode ser extremamente útil para os usuários do Tablet PC. Um exemplo primo é em aplicativos que fornecem superfícies de tinta personalizadas para inserir texto usando uma caneta. As superfícies de tinta personalizada são uma ótima maneira de os aplicativos fornecerem funcionalidades exclusivamente personalizadas específicas às tarefas de entrada de texto de cada aplicativo. Além disso, as superfícies de tinta personalizada fornecem uma experiência de usuário do Tablet PC totalmente integrada, o que torna claro que a caneta é um dispositivo de entrada de primeira classe em aplicativos que as contêm. No entanto, os aplicativos que fornecem superfícies de tinta personalizada podem não permitir ou não podem fornecer o mesmo nível de suporte de correção que está disponível na correção no documento do painel de entrada.

![coletor de tinta personalizado](images/b6797b12-dda6-44c4-87f4-570fe0c23f3a.jpg)

Aplicativos com base em serviços de texto ou habilitados em que a correção no documento é útil para a correção de texto não inserido usando o painel de entrada é capaz de usar a API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) do painel de entrada (classe [Microsoft. TextInput. HandwrittenTextInsertion](/previous-versions/ms573516(v=vs.100)) no código gerenciado) para habilitar a correção no documento para o texto inserido por outros meios. Dessa forma, os aplicativos podem adicionar um suporte avançado à correção para suas superfícies de tinta personalizada ou outros cenários de entrada de texto e arredondar sua história de entrada de texto do Tablet PC. A API do painel de entrada IHandWrittenTextInsertion é incluída como parte do sistema operacional Windows Vista e como parte do SDK da plataforma Tablet versão 1,9 ou mais recente. Uma versão baseada em .NET e COM com base na API está incluída. Habilitar a correção no documento para texto não inserido usando o painel de entrada tem suporte no Windows Vista e mais recente. A correção no documento só está disponível para idiomas latinos e não pode exibir nenhum caractere fora do conjunto de caracteres latinos.

## <a name="how-to-use-the-handwrittentextinsertion-api-in-an-application"></a>Como usar a API HandwrittenTextInsertion em um aplicativo

As alterações necessárias para um aplicativo a fim de integrar a correção no documento no painel de entrada para o texto não inserido usando o painel de entrada e o uso da API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) são simples. Todo o código de entrada de texto personalizado do aplicativo permanece inalterado, exceto para a última etapa. No ponto em que o texto inserido usando uma superfície de tinta personalizada, o reconhecimento de fala ou outros meios deve ser exibido em um campo de texto habilitado para serviços de texto, o aplicativo envia o texto para a interface **IHandWrittenTextInsertion** em vez de enviá-lo diretamente para o campo de texto. O componente de programação do painel de entrada, em seguida, manipula a inserção do texto no campo de texto e no armazenamento de backup de serviços de texto. Ao adicionar o texto ao armazenamento de backup de serviços de texto, o componente de programação do painel de entrada lida com a definição das propriedades de texto exigidas pelo painel de entrada para que a correção no documento seja habilitada para esse texto.

A seção a seguir percorre esse processo em detalhes para um aplicativo C++ usando a versão COM da API do [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) . Há observações em qualquer lugar em que as etapas para usar a versão .NET Framework da API em C \# sejam diferentes para o uso da versão com em C++. A API **HandwrittenTextInsertion** gerenciada inclui uma única interface com, **IHandwrittenTextInsertion**. A definição dessa interface está localizada em PenInputPanel. h e PenInputPanel \_ i.c.

Primeiro, o aplicativo deve usar a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para produzir uma instância de [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) com a ID de classe **CLSID \_ HandwrittenTextInsertion**. Observe que a criação de um objeto **CLSID \_ HandwrittenTextInsertion** terá sucesso somente depois que uma janela for criada e receber o foco, porque até então o armazenamento de backup dos serviços de texto não está ativado. Além disso, se tiptsf.dll não estiver presente no sistema, a função **CoCreateInstance** falhará e retornará **REGDB \_ e \_ CLASSNOTREG**, indicando que não há suporte para a correção no documento do painel de entrada no sistema. Neste ponto, o aplicativo deve continuar sem tentar habilitar a correção no documento do painel de entrada. A instância de **HandwrittenTextInsertion** deve ser acessível a partir do código do aplicativo que manipula a inserção de texto em um campo de texto.

> [!Note]  
> Ao trabalhar com a versão .NET Framework da API, o aplicativo deve adicionar uma instrução using para permitir o acesso ao namespace [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) e, em seguida, criar o objeto diretamente.

 

Em segundo lugar, o código do aplicativo que é responsável por inserir texto em um campo de texto deve ser alterado para que ele não insira mais texto em um campo de texto diretamente, mas chama um ou outro dos dois métodos de inserção de [**IHandwrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion). Se os aplicativos devem optar por chamar [**InsertRecognitionResultsArray**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray) ou [**InsertRecognitionResults**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult) depende se o aplicativo tem as alternativas de reconhecimento para o texto armazenado como uma matriz ou como um objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .

> [!Note]  
> Ao trabalhar em código gerenciado, o objeto de reconhecimento correspondente consumido por InsertRecognitionResultsArray é [RecognitionResult](/previous-versions/ms552537(v=vs.100)). Ambos os métodos consomem os três parâmetros a seguir:

 

-   *alternativas* É uma coleção bidimensional de cadeias de caracteres, armazenada como uma matriz de matrizes ou como um objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) (ou [RecognitionResult](/previous-versions/ms552537(v=vs.100))). Se as alternativas forem armazenadas como uma matriz de matrizes, elas deverão ser passadas como um ponteiro de matriz seguro. Cada entrada na matriz de nível superior é uma lista de alternativas para uma única palavra na inserção. A entrada na posição zero nas submatrizes de alternativas é o texto inserido no campo de texto. As alternativas adicionais (índices de 1 a n em cada submatriz) são armazenadas no armazenamento de backup de serviços de texto e oferecidas ao usuário como opções como parte da correção no documento. Se as alternativas não forem incluídas, o usuário verá "nenhuma sugestão" no lugar da lista de alternativas. Se uma inserção contiver várias palavras com espaços entre elas, cada espaço deverá ser incluído como uma entrada na matriz de nível superior.
-   *idioma* do O [LCID](/previous-versions/ms221397(v=vs.71)) do idioma de entrada que corresponde ao texto contido no parâmetro *alternativo* . No caso em que o conteúdo das *alternativas* foi gerado por um reconhecedor de manuscrito ou de fala, essa também é a propriedade [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) associada ao Recognizer usado.
-   *fLatticeContainsAutoSpacingInformation* Um sinalizador que indica se o texto contido no parâmetro *Alternate* foi gerado por um reconhecedor com espaçamento automático habilitado. Se o espaçamento automático tiver sido habilitado, o sinalizador deverá ser definido como **true**. Se o espaçamento automático tiver sido desabilitado, o sinalizador deverá ser definido como **false**. No caso em que o conteúdo das *alternativas* foi gerado por um reconhecedor que não oferece suporte ao espaçamento automático ou não foi gerado por um reconhecedor, o sinalizador deve ser definido como **false**.

O modelo de programação do painel de entrada é capaz de inserir o texto no documento ou aplicativo da posição do cursor do sistema.

Os dois métodos retornarão **S \_ OK** se a inserção for realizada com sucesso. Eles retornam **e \_ nointerface** se o aplicativo não for baseado em serviços de texto ou habilitados, e **e \_ INVALIDARG** se as *alternativas* estiverem formatadas incorretamente ou inacessíveis. Eles também podem retornar **E \_ OUTOFMEMORY** se não houver memória suficiente disponível no sistema ou **E \_ falhar** após uma falha catastrófica, como a estrutura de serviços de texto não estar habilitada.

### <a name="conclusion"></a>Conclusão

Habilitar a correção no documento no painel de entrada para texto não inserido usando o painel de entrada é uma maneira barata e fácil de um aplicativo baseado em serviços de texto ou habilitado para complementar um método de entrada ou de tinta personalizado com funcionalidade avançada de correção baseada em caneta. No Windows Vista, todos os aplicativos de edição avançada e Trident são habilitados para serviços de texto. Embora as superfícies de tinta integradas sejam uma ótima opção para adicionar uma experiência de usuário personalizada do Tablet PC a um aplicativo, elas só dão suporte à metade da entrada de texto se não incluírem recursos de correção. A correção no documento fornece aos usuários a outra metade da história, adicionando a capacidade de trocar uma seleção por uma alternativa de reconhecimento ou de reescrever parte ou toda a seleção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Programando o painel de entrada de texto](programming-the-text-input-panel.md)
</dt> </dl>

 

 
