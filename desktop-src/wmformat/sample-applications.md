---
title: Windows Aplicativos de exemplo do SDK do formato de mídia
description: Windows Aplicativos de exemplo do SDK do formato de mídia
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows SDK de formato de mídia, aplicativos de exemplo
- DRM (gerenciamento de direitos digitais), aplicativos de exemplo
- DRM (gerenciamento de direitos digitais), aplicativos de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c778ef1613359f6f3dc6c08d918e32f2f29bade
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475002"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Windows Aplicativos de exemplo do SDK do formato de mídia

o código de exemplo fornecido com esse SDK está na forma de projetos para Microsoft Visual Studio 2005. A maioria dos exemplos está em C++, mas ManagedWMFSDKWrapper e ManagedMetadataEdit exigem C#.

esses exemplos não funcionarão a menos que o sdk do formato de mídia Windows ou o sdk do Windows Player tenha sido instalado.

As informações de uso de cada exemplo estão contidas em um arquivo de readme.txt em cada diretório de exemplo.




| Samle | Descrição | 
|-------|-------------|
| AudioPlayer | reproduz Windows arquivos de mídia incluindo arquivos protegidos por DRM. Ele é controlado por meio de uma GUI, e os comandos incluem reproduzir, pausar, buscar e parar. Ele pode reproduzir arquivos locais ou arquivos lidos da Internet (incluindo as saídas para a Internet usando o exemplo WMVNetWrite).<blockquote>[!Note]<br />As partes de DRM deste exemplo não têm suporte em versões baseadas em x64 do Windows.</blockquote><br /> | 
| DRMHeader | DRMHeader é um aplicativo de console que usa a interface <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> do editor de metadados para ler atributos DRM de arquivos sem vincular à biblioteca estática do DRM.<blockquote>[!Note]<br />Não há suporte para este exemplo em versões baseadas em x64 do Windows.</blockquote><br /> | 
| DRMShow | DRMShow é um aplicativo de console que mostra como ler as propriedades de <a href="wmformat-glossary.md"><em>DRM</em></a> de um arquivo de mídia Windows usando o método <strong>IWMDRMReader:: GetDRMProperty</strong> . Este exemplo demonstra o uso do método <strong>IWMDRMReader:: GetDRMProperty</strong> e as propriedades que podem ser recuperadas do leitor de DRM. Ele não demonstra como adquirir uma licença para conteúdo protegido por DRM. Este exemplo requer que a biblioteca de stub de DRM WMStubDRM. lib seja compilada.<br /><blockquote>[!Note]<br />Não há suporte para este exemplo em versões baseadas em x64 do Windows.</blockquote><br /> Ao adquirir o WMStubDRM. lib da Microsoft, o nível de segurança do aplicativo é atribuído à biblioteca. Se o nível de segurança da biblioteca que você recebe não for suficiente para reproduzir um arquivo protegido, este exemplo exibirá um erro.<br /> | 
| DirectShowInterop/DSCopy | codifica um ou mais arquivos em um arquivo ASF usando o filtro de gravador ASF do DirectShow WM. O arquivo de entrada pode ser qualquer formato compactado ou descompactado com suporte pelo DirectShow. | 
| DirectShowInterop/DSPlay | Este exemplo é um player de arquivo de mídia de áudio/vídeo interativo com suporte a <a href="wmformat-glossary.md"><em>DRM</em></a> . ele usa o filtro de leitor ASF do WM DirectShow para reproduzir Windows arquivos de mídia (ASF, WMA, WMV) sem proteção de drm e arquivos que usam o drm em um nível de 100 ou abaixo. Consulte readme.txt no diretório da amostra para obter mais informações. | 
| DirectShowInterop/DSSeekFm | este exemplo demonstra como usar o filtro de leitor asf do DirectShow WM para reproduzir conteúdo ASF em um grafo de filtro de DirectShow e também como usar o suporte à busca de quadros no SDK do formato de mídia do Windows. | 
| Gerenciado/WMFSDKWrapper | Esse assembly gerenciado serve como um wrapper usado por exemplos de código gerenciado para acessar algumas interfaces de metadados deste SDK. | 
| Gerenciado/MetadataEdit | esse aplicativo C# pode ser usado para exibir e editar metadados de arquivos de mídia Windows. | 
| MetaDataEdit | Esta é uma versão em C++ do aplicativo MetadataEdit gerenciado. | 
| ReadFromStream | Este exemplo de aplicativo de console mostra como ler dados de <strong>IStream</strong> com WMReader. a origem de <strong>IStream</strong> foi implementada para usar um arquivo no formato de mídia Windows (WMA/WMV/ASF).<blockquote>[!Note]<br />Este exemplo não mostra como processar os exemplos de mídia provenientes do WMReader. para obter exemplos de como processar áudio/vídeo ou outros tipos de amostras de mídia, consulte outros exemplos, por exemplo, AudioPlayer, que estão incluídos no SDK do formato de mídia Windows.</blockquote><br /> | 
| UncompAVIToWMV | Este exemplo de aplicativo de console mostra o código necessário para compactar um arquivo AVI para um arquivo WMV. Ele mostra como mesclar exemplos de fluxos de áudio e vídeo de vários arquivos AVI e mesclá-los em fluxos semelhantes ou criar um novo fluxo com base no perfil de fluxo de origem. Ele também mostra como criar um fluxo arbitrário, executar a codificação de passagem, adicionar o código de tempo SMPTE e aplicar a proteção DRM versão 1. | 
| WMGenProfile/exe | Este exemplo foi atualizado a partir da versão 7,1. Agora é um aplicativo de caixa de diálogo do MFC. O exemplo de WMGenProfile demonstra o uso da biblioteca estática WMGenProfile. Ele também serve como uma ferramenta para a criação de perfis. essa ferramenta destina-se a desenvolvedores familiarizados com o formato de mídia Windows. A IU não foi testada quanto à experiência do usuário e não se destina a uma recomendação sobre como apresentar essas informações a um usuário. | 
| WMGenProfile/lib | O exemplo da biblioteca GenProfile demonstra a criação de perfis. Ele mostra como criar tipos de mídia e fluxos para vários tipos de fluxo (áudio, vídeo, script, imagem, transferência de arquivo e Web). ele não demonstra como trabalhar com perfis de sistema ou como converter perfis de sistema em perfis que especificam os codecs de Windows Media Audio e vídeo 9 Series. | 
| WMProp | Este aplicativo de console demonstra como recuperar atributos usando o objeto do editor de metadados e as informações de perfil do leitor. | 
| WMStats | Esse aplicativo de console exibe as estatísticas de leitor e gravador. Várias instâncias do WMStats também podem ser usadas simultaneamente em uma máquina. Inicie uma instância como um servidor para enviar o fluxo para a rede e, em seguida, execute uma segunda instância como um cliente para verificar se o servidor está transmitindo corretamente. | 
| WMSyncReader | Este exemplo de aplicativo de console mostra como ler um arquivo de mídia usando <strong>IWMSyncReader</strong> sem criar nenhum thread extra ou usar retornos de chamada. Os seguintes recursos são implementados: lendo amostras compactadas ou descompactadas<br /> Busca baseada em tempo<br /> Busca baseada em quadros<br />Fonte derivada de <strong>IStream</strong><br /> | 
| WMVAppend | esse aplicativo de console usa dois arquivos de mídia Windows para entrada e tenta criar um arquivo de saída com o conteúdo do primeiro seguido pelo segundo. O exemplo compara os perfis dos dois arquivos de entrada para garantir que eles sejam semelhantes o suficiente para serem acrescentados. Se esse não for o caso, será exibida uma mensagem de erro. Por exemplo, uma mensagem de erro ocorre quando um arquivo é somente áudio e o segundo é um arquivo de vídeo de áudio ou quando dois arquivos de áudio têm taxas de bits diferentes. O exemplo aceita fontes de taxa de bits variável (VBR). No entanto, ao comparar os perfis das duas fontes de VBR, o exemplo ignora a diferença média da taxa de bits, pois dois fluxos de VBR terão taxas de bits médias diferentes, mesmo que tenham sido criados usando o mesmo perfil. WMVAppend não pode comparar a taxa de bits de pico de fluxos de VBR de taxa de bits não restritos, ou o nível de qualidade de fluxos de VBR com base em qualidade, porque essas informações não existem nos arquivos de origem. Portanto, é responsabilidade do usuário certificar-se de que dois arquivos de origem sejam criados usando o mesmo perfil. Caso contrário, o conteúdo inválido poderá ser criado.<br /> | 
| WMVCopy | Este exemplo mostra o código necessário para copiar um arquivo WMV. Ele mostra como ler e gravar exemplos compactados, ler scripts e atributos de cabeçalho e modificar atributos de cabeçalho. | 
| WMVNetWrite | esse aplicativo de console mostra como um arquivo de mídia Windows é transmitido pela Internet. O exemplo requer que uma porta seja especificada e, em seguida, o arquivo pode ser reproduzido usando um player. | 
| WMVRecompress | Este aplicativo de console mostra como recompactar um arquivo WMV. Ele demonstra a leitura de amostras não compactadas, a gravação de amostras descompactadas e a codificação de várias passagens, a saída de vários canais e a recompactação inteligente. | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**sobre o SDK do formato de mídia Windows**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 





