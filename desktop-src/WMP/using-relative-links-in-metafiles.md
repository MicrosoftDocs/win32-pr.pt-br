---
title: Usando links relativos em metaarquivos
description: Usando links relativos em metaarquivos
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Playlists do metarquivo do Windows Media, links relativos
- listas de reprodução, links relativos
- listas de reprodução de metarquivo, links relativos
- metaarquivos, links relativos
- Metaarquivos do Windows Media, links relativos
- links relativos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822481"
---
# <a name="using-relative-links-in-metafiles"></a>Usando links relativos em metaarquivos

Links relativos são um recurso totalmente suportado de metaarquivos do Windows Media. Você pode usar links relativos em metaarquivos da mesma forma que os usa em documentos HTML. O uso de links relativos permite criar metarquivos que são portáteis, o que significa que você pode copiar ou mover uma estrutura de diretório inteira para outro servidor sem Atualizar os caminhos para arquivos gráficos usados como faixas ou os atributos **href** de elementos **moreinfo** (se eles fizerem referência a arquivos no mesmo servidor Web que o metarquivo armazenado). Os links relativos funcionam, em qualquer aplicativo que ofereça suporte a eles, porque as partes da URL não incluídas no atributo **href** de um elemento são incluídas na URL enviada pelo aplicativo para o servidor quando essa URL é solicitada. Isso significa que o protocolo (como https://), o nome do servidor e o diretório virtual no qual o arquivo que contém o link relativo está localizado são todos incluídos na URL que é enviada ao servidor. Se o arquivo de mídia ou URL ao qual você vincular usando um link relativo não residir no mesmo servidor que o metarquivo, o link relativo não será válido.

> [!Note]  
> Essas informações sobre links relativos só estão corretas quando se usa um link para os metaarquivos que são abertos no Windows Media Player autônomo. Quando você usa o controle incorporado do Windows Media Player, todos os links são relativos à página na qual o controle está hospedado, a menos que o elemento filho **base** do elemento **ASX** seja usado para redirecionar o caminho relativo.

 

Todos os links relativos no metarquivo devem ser totalmente relativos, não relativos à unidade, para mídia de streaming. Quando uma URL começa com um \\ caractere "", o link é relativo à unidade. O Windows Media Player tenta abrir o arquivo vinculado ao na unidade em que o metarquivo foi aberto, geralmente um servidor Web. Como os servidores Web usam diretórios virtuais, o Windows Media Player tenta localizar o fluxo especificado ou o arquivo de mídia em um subdiretório de um diretório virtual no servidor Web onde o metarquivo foi aberto. Um usuário não teria acesso a um diretório de servidor. O exemplo nesta seção ilustra o uso de um link totalmente relativo.

Você pode usar links relativos à unidade ao usar metarquivos em um único computador onde todos os arquivos de mídia vinculados à lista de reprodução de metarquivo existem em um dispositivo de armazenamento nesse computador. No entanto, não é possível transmitir mídia dessa maneira.

Quando você usa um link para outro metarquivo para permitir links relativos, o nome exibido como o título pelo Windows Media Player é o título no metarquivo original.

Links relativos não podem ser usados para URLs para um servidor de mídia de streaming porque diferentes protocolos são usados para acessar conteúdo de streaming de mídia.

Na playlist de exemplo a seguir, o primeiro **ENTRYREF** contém uma URL para outra playlist, relativa. Wax.


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



O exemplo a seguir é o arquivo Relative. Wax, que contém links relativos.


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



A URL que contém a referência à playlist, relativa. Wax, pode existir em uma lista de reprodução de metarquivo em qualquer lugar que possa ser acessada pelo usuário. Para que a URL seja processada com êxito, deve haver um servidor Web chamado "example.microsoft.com". Esse servidor Web deve ter um diretório virtual definido como "Metafiles". A lista de reprodução referenciada, relativa. Wax, deve existir no servidor Web chamado "example.microsoft.com" no diretório virtual "Metafiles".

Para os arquivos de mídia referenciados na playlist relativa. Wax a ser acessado e reproduzido com êxito, deve haver um diretório chamado "Graphics", que é um subdiretório do "Metafiles" do diretório virtual do servidor. O arquivo de gráficos Logo1.jpg, referenciado no elemento **banner** , deve ser o subdiretório chamado Graphics.

Da mesma forma, um documento chamado Category1.htm deve residir em um subdiretório chamado Category1. O diretório chamado Category1 deve existir como um subdiretório dos "metaarquivos" do diretório virtual no servidor Web example.microsoft.com.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




