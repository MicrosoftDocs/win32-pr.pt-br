---
title: Coleções de fontes personalizadas (Windows 7/8)
description: O DirectWrite fornece acesso à coleção de fontes do sistema usando o método IDWriteFactory GetSystemFontCollection.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa764330f27b72051ef682c6ce5f1176c42c7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641445"
---
# <a name="custom-font-collections-windows-78"></a>Coleções de fontes personalizadas (Windows 7/8)

O [DirectWrite](direct-write-portal.md) fornece acesso à coleção de fontes do sistema usando o método [**IDWriteFactory:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Essa é a coleção de fontes usada com mais frequência. No entanto, alguns aplicativos precisam usar fontes que não estão instaladas no sistema, como de arquivos de fonte incluídos ou arquivos de fonte inseridos no aplicativo.

Se as fontes desejadas não estiverem na coleção de fontes do sistema, você poderá criar uma coleção de fontes personalizada derivada de [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection).

Esta visão geral consiste nas seguintes partes:

-   [Registrando e cancelando o registro de um carregador de coleção de fontes](#registering-and-unregistering-a-font-collection-loader)
-   [IDWriteFontCollectionLoader](#idwritefontcollectionloader)
-   [IDWriteFontFileEnumerator](#idwritefontfileenumerator)
-   [CreateCustomFontFileReference](#createcustomfontfilereference)
-   [IDWriteFontFileLoader](#idwritefontfileloader)
-   [IDWriteFontFileStream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Registrando e cancelando o registro de um carregador de coleção de fontes

Você registra um carregador de coleção de fontes usando o método [**IDWriteFactory:: RegisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) e passando a ele uma interface [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementada pelo aplicativo como um objeto singleton. Esse objeto carregará as fontes quando a coleção personalizada for solicitada. A coleção de fontes do sistema e as coleções de fontes personalizadas são armazenadas em cache, portanto, as fontes são carregadas apenas uma vez.

O carregador da coleção de fontes deve ser descarregado eventualmente usando [**IDWriteFactory:: UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader).

> [!Note]  
> O registro do carregador da coleção de fontes é adicionado à contagem de referência; Não chame [**UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) de dentro do destruidor ou o objeto do carregador da coleção nunca terá o seu registro cancelado.

 

## <a name="idwritefontcollectionloader"></a>IDWriteFontCollectionLoader

Crie um objeto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) usando [**IDWriteFactory:: CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) e passando-o para uma chave definida pelo aplicativo. A chave é um ponteiro void e o tipo de dados, o formato e o significado são definidos pelo aplicativo e são opacos para o sistema de fontes.

Enquanto que a chave pode ser qualquer coisa, [DirectWrite](direct-write-portal.md) exige que cada chave seja:

-   Exclusivo para uma única coleção de fontes dentro do escopo do carregador.
-   Válido até que o carregador tenha o registro cancelado usando a fábrica.

Quando o método [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) é chamado, [DirectWrite](direct-write-portal.md) chama de volta para uma interface [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implementada como um objeto singleton pelo aplicativo. O método de retorno de chamada [**IDWriteFontCollectionLoader:: CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) é usado pelo DirectWrite para recuperar um objeto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) implementado pelo aplicativo. O objeto [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) que está sendo usado para criar a coleção é passado para esse método e deve ser usado pelo enumerador de arquivo de fonte para criar os objetos [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) a serem incluídos na coleção.

A chave passada para esse método identifica a coleção de fontes e é a mesma chave passada para [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection).

## <a name="idwritefontfileenumerator"></a>IDWriteFontFileEnumerator

O objeto [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) definido pelo aplicativo que foi criado pelo método [**CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) é usado para enumerar os arquivos de fonte em uma coleção, criando um objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) para cada arquivo. O método [**IDWriteFontFileEnumerator:: MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) altera a posição para o próximo arquivo de fonte. Se houver um arquivo na posição, ele definirá *hasCurrentFile* como **true**. Caso contrário, ele será definido como **false** e o método retornará **S \_ OK**.

> [!Note]  
> O enumerador de arquivo de fonte deve iniciar posicionado antes do primeiro elemento e avançado na primeira chamada para [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext).

 

Um objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) é apresentado pelo método [**IDWriteFontFileEnumerator:: GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) . Se não houver nenhum arquivo de fonte na posição atual, porque [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) ainda não foi chamado ou hasCurrentFile foi definido como **false**, então **GetCurrentFontFile** retornará **E \_ falhará**.

## <a name="createcustomfontfilereference"></a>CreateCustomFontFileReference

A saída do objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) por [**GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) pode ser criada chamando [**IDWriteFactory:: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference). A chave de referência do arquivo de fonte identifica uma referência de arquivo de fonte específica e deve ser exclusiva no carregador de arquivo de fonte que carregará o arquivo.

## <a name="idwritefontfileloader"></a>IDWriteFontFileLoader

O método [**CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) usa um objeto [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) implementado pelo aplicativo que é usado para carregar a fonte. O método de retorno de chamada [**IDWriteFontFileLoader:: CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) é passado à chave e gera um objeto [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) .

## <a name="idwritefontfilestream"></a>IDWriteFontFileStream

O objeto [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) implementado pelo aplicativo fornece os dados do arquivo de fonte para uma referência de arquivo de fonte de um carregador de arquivo de fonte personalizado. Junto com o tamanho do arquivo e a hora da última gravação, ele fornece um método ([**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) para recuperar fragmentos de arquivo que devem ser compilados em um objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) .

> [!Note]  
> As implementações de [**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) devem retornar um erro se o fragmento solicitado estiver fora dos limites do arquivo.

 

Um [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) pode obter o conteúdo do arquivo de fonte de qualquer lugar, como a unidade de disco rígido local ou recursos incorporados.

 

 