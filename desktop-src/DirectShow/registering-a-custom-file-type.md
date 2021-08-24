---
description: este artigo descreve como o gerenciador de Graph de filtro localiza um filtro de origem, dado um nome de arquivo.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registrando um tipo de arquivo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2815748fafaff3e2d20d0de1ab5fa0bcc9dec62f4e65ffbdd8479fec434d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697046"
---
# <a name="registering-a-custom-file-type"></a>Registrando um tipo de arquivo personalizado

este artigo descreve como o gerenciador de Graph de filtro localiza um filtro de origem, dado um nome de arquivo. Você pode usar esse mecanismo para registrar seus próprios tipos de arquivo personalizados. depois que o tipo de arquivo for registrado, DirectShow carregará automaticamente o filtro de origem correto sempre que um aplicativo chamar [**IGraphBuilder:: renderfile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

-   [Visão geral](#overview)
-   [Protocolos](#protocols)
-   [Extensões de arquivo](#file-extensions)
-   [Verificar bytes](#check-bytes)
-   [Carregando o filtro de origem](#loading-the-source-filter)
-   [Tipos de arquivo personalizados no Windows Media Player](#custom-file-types-in-windows-media-player)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

para localizar um filtro de origem de um determinado nome de arquivo, o filtro Graph Manager tenta fazer o seguinte, na ordem:

1.  Corresponder ao protocolo, se houver.
2.  Corresponder à extensão do arquivo.
3.  Corresponder padrões de bytes no arquivo, chamado *verificar bytes*.

## <a name="protocols"></a>Protocolos

Os nomes de protocolo, como "FTP" ou "http", são registrados no

**\_raiz de classes hKey \_**

, com a seguinte estrutura:


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



se o nome do arquivo ou a URL contiver dois-pontos (': '), o filtro Graph Manager tentará usar a parte antes de ': ' como um nome de protocolo. Por exemplo, se o nome for "myprot://myfile.ext", ele pesquisará uma chave do registro chamada **myprot**. se essa chave existir e contiver uma subchave chamada "Extensions", o filtro Graph Manager pesquisará dentro dessa subchave para entradas que correspondam à extensão do arquivo. O valor da chave deve ser um GUID na forma de cadeia de caracteres; por exemplo, " {00000000-0000-0000-0000-000000000000} ". se o filtro Graph gerenciador não puder corresponder a nada dentro da subchave **extensões** , ele procurará uma subchave chamada **filtro de origem**, que também deve ser um GUID no formato de cadeia de caracteres.

se o filtro Graph Manager encontrar um GUID correspondente, ele o usará como o CLSID do filtro de origem e tentará carregar o filtro. Se não encontrar uma correspondência, ela usará o filtro de [origem do arquivo (URL)](file-source--url--filter.md) , que trata o nome do arquivo como uma URL.

Há duas exceções a esse algoritmo:

-   Para excluir letras de driver, as cadeias de caracteres de caractere único não são consideradas protocolos.
-   Se a cadeia de caracteres for "file:" ou "file://", ela não será tratada como um protocolo.

## <a name="file-extensions"></a>Extensões de arquivo

se não houver nenhum protocolo no nome do arquivo, o filtro Graph Manager procurará entradas com as **\_ \_ \\ \\ extensões \\ da chave HKEY CLASSES do tipo de mídia raiz**.*ext* \\ , em que.*ext* é a extensão de arquivo. Se essa chave existir, o **filtro de origem** de valor conterá o CLSID do filtro de origem, em forma de cadeia de caracteres. Opcionalmente, a chave pode ter valores para **tipo de mídia** e **subtipo**, que fornecem os GUIDs de tipo e subtipo principais.

## <a name="check-bytes"></a>Verificar bytes

Alguns tipos de arquivo podem ser identificados por padrões específicos de bits que ocorrem em deslocamentos de byte específicos no arquivo. o filtro Graph Manager procura as chaves no registro com o seguinte formato:

**HKEY \_ \_ \\ MediaType \\ raiz de classes**{ *tipo principal* } \\ { *subtipo* }

onde o *tipo principal* e *SUBtipo* são GUIDs que definem o tipo de mídia para o fluxo de bytes. Cada chave contém uma ou mais subchaves, geralmente denominadas 1, 2 e assim por diante, que definem os bytes de verificação; e uma subchave chamada **filtro de origem** que fornece o CLSID do filtro de origem, em forma de cadeia de caracteres. As subchaves de byte de verificação são cadeias de caracteres que contêm um ou mais quádruplos de números chamados:

*offset*, *CB*, *máscara*, *Val*

para corresponder ao arquivo, o filtro Graph Manager lê os bytes de cb, começando do deslocamento de número de byte. Em seguida, ele executa uma e-bit em relação ao valor em Mask. Se o resultado for igual a Val, o arquivo será uma correspondência para esse Quad. Os valores Mask e Val são fornecidos em Hex. Uma entrada em branco para Mask é tratada como uma cadeia de 1s de comprimento de CB. Um valor negativo para deslocamento indica um deslocamento do final do arquivo. Para corresponder à chave, o arquivo deve corresponder a todos os quatro quádruplos em qualquer uma das subchaves.

Por exemplo, suponha que o registro contenha as seguintes chaves em **\\ tipo de mídia de HKCR**:


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



A primeira chave corresponde ao fluxo de MEDIATYPE do tipo principal \_ . A subchave abaixo corresponde à MIDI de MEDIATYPE de subtipo \_ . O valor da subchave de filtro de origem é CLSID \_ AsyncReader, CLSID do filtro de [origem de arquivo (Async)](file-source--async--filter.md) .

Cada entrada pode ter vários quádruplos; todos eles devem corresponder. No exemplo a seguir, os quatro primeiros bytes do arquivo devem ser 0xAB, 0xCD, 0x12, 0x34; e os últimos 4 bytes do arquivo devem ser 0xAB, 0xAB, 0x00, 0xAB:


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



Além disso, pode haver várias entradas listadas em um único tipo de mídia. Uma correspondência a qualquer um deles é suficiente. Esse esquema permite um conjunto de máscaras alternativas; por exemplo, arquivos. wav que podem ou não ter um cabeçalho RIFF.

> [!Note]  
> Esse esquema é semelhante ao usado pela função [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) .

 

## <a name="loading-the-source-filter"></a>Carregando o filtro de origem

supondo que o filtro Graph Manager localize um filtro de origem correspondente para o arquivo, ele adiciona esse filtro ao grafo, consulta o filtro para a interface [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) e chama [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load). Os argumentos para o método **Load** são o nome do arquivo e o tipo de mídia, conforme determinado no registro.

se o filtro Graph gerenciador não conseguir localizar nada do registro, o padrão será usar o filtro de origem de arquivo assíncrono. Nesse caso, ele define o tipo de mídia para **\_ fluxo de MediaType**, **MEDIASUBTYPE \_ None**.

## <a name="custom-file-types-in-windows-media-player"></a>Tipos de arquivo personalizados no Windows Media Player

Windows Media Player usa um conjunto adicional de entradas do registro. para obter mais informações, consulte [registro de extensão de nome de arquivo Configurações](../wmp/file-name-extension-registry-settings.md) no SDK do Windows Media Player.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[gravando filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 
