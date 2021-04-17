---
title: Sobre os serviços de biblioteca
description: Sobre os serviços de biblioteca
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, sobre
- Biblioteca do Windows Media Player, serviços
- biblioteca, serviços
- biblioteca, sobre
- versões do Windows Media Player, serviços de biblioteca
- enumerações, serviços de biblioteca
- eventos, serviços de biblioteca
- exemplos, serviços de biblioteca
- interfaces, serviços de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743efc8ae5cb464aa38655314c52112bc9541de6
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105784927"
---
# <a name="about-library-services"></a>Sobre os serviços de biblioteca

Em versões anteriores do Windows Media Player, o software usava um banco de dados de biblioteca única para cada usuário. Esse banco de dados foi armazenado no computador do usuário e estava associado conceitualmente ao usuário e a uma instância específica do Player.

O Windows Media Player 11 apresenta os conceitos de várias bibliotecas remotas. Agora, além de sua biblioteca padrão ou *local*, o Windows Media Player pode exibir o conteúdo recuperado de bibliotecas em outros computadores conectados a uma rede, o que pode incluir outros usuários conectados ao mesmo computador. O Player também pode exibir exibições de biblioteca de outras fontes, como dispositivos habilitados para MTP ou CDs de dados. Da perspectiva do usuário final, isso significa que o conteúdo de mídia digital localizado em vários locais diferentes pode ser gerenciado de vários locais usando a mesma interface do usuário familiar do Windows Media Player. Da perspectiva do desenvolvedor, isso significa que você pode usar as interfaces COM do SDK do Windows Media Player para enumerar as bibliotecas disponíveis e, em seguida, usá-las, como você usou a biblioteca local em versões anteriores.

Para enumerar as bibliotecas disponíveis, use a interface **IWMPLibraryServices** . Essa interface expõe o método [IWMPLibraryServices:: getCountByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) , que recupera a contagem de bibliotecas de um determinado tipo. Os tipos de biblioteca são definidos pela enumeração [WMPLibraryType](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) . Essa enumeração inclui um valor para a biblioteca local, wmpltLocal. Isso ocorre porque o recurso serviços de biblioteca sempre permite que você trabalhe com a biblioteca local usando **IWMPLibraryServices** e as interfaces relacionadas.

> [!Note]  
> A enumeração **WMPLibraryType** inclui o valor wmpltRemote, que representa as bibliotecas de mídia compartilhadas pela rede. Para acessar essas bibliotecas compartilhadas, o controle do Player deve estar em execução no modo remoto. Para obter informações sobre como executar o controle Player no modo remoto, consulte [comunicação remota do controle do Windows Media Player](remoting-the-windows-media-player-control.md).

 

Depois de recuperar a contagem de bibliotecas, você pode iterar a coleção de bibliotecas disponíveis chamando repetidamente [IWMPLibraryServices:: getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) em um loop, passando um novo valor de índice com cada iteração. Esse método recupera um ponteiro para uma interface [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) , que representa a biblioteca individual.

Depois de recuperar um ponteiro para **IWMPLibrary**, você pode chamar [IWMPLibrary:: get \_ mediacollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) para recuperar um ponteiro para uma interface **IWMPMediaCollection** . Com esse ponteiro de interface, você pode trabalhar com uma biblioteca individual da mesma forma que usaria a biblioteca local. Você também pode recuperar uma cadeia de caracteres que contém o nome da biblioteca chamando [IWMPLibrary:: get \_ Name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name), que será útil se você precisar exibir o nome da biblioteca para o usuário. Você pode chamar [IWMPLibrary:: get \_](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) para obter o **WMPLibraryType** de uma biblioteca específica.

Você pode manipular o evento [IWMPEvents3:: LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) para saber quando uma biblioteca se torna disponível e o evento [IWMPEvents3:: LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) para saber quando uma biblioteca se desconecta. Cada um desses eventos fornece um ponteiro **IWMPLibrary** que representa a biblioteca conectada ou desconectada. Você pode chamar [IWMPLibrary:: isidêntico](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) para determinar se a biblioteca conectada ou desconectada é uma biblioteca que você está usando no momento.

Há algumas diferenças importantes quando você trabalha com uma biblioteca recuperada por meio da interface **IWMPLibraryServices** em comparação com o trabalho com uma biblioteca recuperada usando [IWMPCore:: get \_ mediacollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection). As seguintes diferenças aplicam:

-   Normalmente, você pode recuperar resultados da consulta muito mais rapidamente das bibliotecas recuperadas por meio do **IWMPLibraryServices**. (Isso pressupõe que outros fatores, como tempos de acesso de rede e disco rígido, sejam iguais.)
-   A lista de atributos de metadados de item de mídia disponíveis em bibliotecas recuperadas por meio de **IWMPLibraryServices** geralmente é um subconjunto daqueles disponíveis na biblioteca local recuperada por meio de [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore).
-   Se você recuperar a biblioteca local por meio de **IWMPLibraryServices**, todos os mesmos atributos estarão disponíveis para seu uso como aqueles disponíveis quando você recuperar a biblioteca local por meio do **IWMPCore**. No entanto, você poderá recuperar os resultados da consulta muito mais rapidamente para os atributos mais usados.
-   Você deve usar coleções de cadeia de caracteres para criar elementos de interface do usuário ao trabalhar com bibliotecas recuperadas por meio de **IWMPLibraryServices**. Por exemplo, [IWMPMediaCollection2:: getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) permite que você use uma consulta personalizada (representada pela interface **IWMPQuery** ) para recuperar uma coleção de cadeias de caracteres.
-   Bibliotecas remotas recuperadas por meio da interface **IWMPLibraryServices** talvez nem sempre estejam conectadas à instância do Player atual. Isso significa que é importante manipular os eventos **LibraryConnect** e **LibraryDisconnect** para saber quando a disponibilidade da biblioteca é alterada e para manipular o evento [IWMPEvents3:: StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) para saber quando as cadeias de caracteres são adicionadas ou removidas das coleções de cadeias que você usa para exibir elementos da interface do usuário. Você também deve manipular eventos **StringCollectionChange** para a biblioteca local por motivos semelhantes.

É importante entender que as coleções de cadeias de caracteres de uma determinada biblioteca podem ser alteradas a qualquer momento. Uma coleção de cadeia de caracteres pode estar vazia quando você a recupera pela primeira vez, como no caso de uma biblioteca conectada recentemente, mas o Player ainda não tiver enumerado seu conteúdo. Por outro lado, uma coleção de cadeia de caracteres já pode conter todas as informações de que você precisa. Nesse caso, você pode nunca receber um evento **StringCollectionChange** porque o conteúdo da biblioteca tinha sido completamente enumerado antes de você criar a consulta e nada mais está mudando.

Portanto, para manter a interface do usuário atual, você deve enumerar o conteúdo da coleção de cadeias de caracteres ao recuperar a interface **IWMPStringCollection** e manipular o evento **StringCollectionChange** para saber mais sobre as atualizações quando elas ocorrerem.

## <a name="sample"></a>Amostra

O exemplo chamado WMPML demonstra como trabalhar com serviços de biblioteca. Para obter mais informações sobre exemplos do SDK do Windows Media Player, consulte [exemplos](samples.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a biblioteca**](about-the-library.md)
</dt> <dt>

[**Sobre o objeto de consulta**](about-the-query-object.md)
</dt> <dt>

[**Interface IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Interface IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[**Interface IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Interface IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[**Interface IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[**Interface IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[**Interface IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Trabalhando com a biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




