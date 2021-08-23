---
title: Descompactação de Image-Data
description: Descompactação de Image-Data
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- VCM (Gerenciador de compactação de vídeo), descompactação de dados de imagem
- VCM (Gerenciador de compactação de vídeo), descompactação de dados de imagem
- Funções ICDecompressEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5006a019fd3fcf24a08f620186af8eb09d9516e103722395ed96722b48696cb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495596"
---
# <a name="image-data-decompression"></a>Descompactação de Image-Data

Seu aplicativo usa uma série de funções [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) para controlar o descompactador. As funções podem ajudá-lo a executar as seguintes tarefas:

-   Selecione um descompactador.
-   Prepare o descompactador.
-   Descompacte os dados.
-   Encerrar descompactação.

Seu aplicativo lida com a descompactação da mesma forma que manipula a compactação, exceto que o formato de entrada é um formato compactado e o formato de saída é um formato que é exibível. O formato de entrada para descompactação geralmente é obtido do cabeçalho do fluxo. Depois de determinar o formato de entrada, seu aplicativo pode usar as funções [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) ou [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) para encontrar um descompactador que possa tratá-lo.

As funções e macros do [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) são um superconjunto do grupo de funções do [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) e fornecem mais recursos. A funcionalidade de **ICDecompressEx**, [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin), [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)e [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) substitui a das funções **ICDecompress**, [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin), [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)e [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) . Use as funções e macros do **ICDecompressEx** no lugar dos equivalentes do **ICDecompress** .

## <a name="decompressor-and-decompression-format-selection"></a>Seleção de formato de descompactação e descompressão

Se desejar descompactar dados e seu aplicativo exigir um formato de saída específico, você poderá usar a função [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) para consultar o descompactador para determinar se ele dá suporte aos formatos de entrada e saída.

Se o formato de saída não for importante em seu aplicativo, você precisará localizar apenas um descompactador que possa manipular o formato de entrada. Para determinar se um descompactador pode manipular o formato de entrada, use [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) e especifique **NULL** para o parâmetro *lpbiDst* . seu aplicativo pode determinar o tamanho do buffer necessário para os dados que especificam o formato de descompactação enviando a mensagem [**ICM \_ descompactar \_ GET \_ format**](icm-decompress-get-format.md) (ou usar a macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) ). você também pode enviar **ICM \_ descompactar o \_ \_ formato GET** (ou a macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) ) para recuperar os dados de formato. O descompactador retorna seu formato sugerido em uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Esse formato normalmente preserva a maioria das informações durante a descompactação. Seu aplicativo deve garantir que o descompactador retorne com êxito antes de descompactar as informações.

Como seu aplicativo aloca a memória necessária para descompactação, ele precisa determinar a memória máxima que o descompactador pode exigir para o formato de saída. a **ICM \_ descompactar \_ obter \_** mensagem de formato obtém o número de bytes que o descompactador usa para o formato padrão.

Se seu aplicativo define seu próprio formato usando [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery), ele também deve obter uma paleta para o bitmap; **ICDecompressExQuery** não fornece definições de paleta. (A maioria dos aplicativos usa formatos padrão e não precisa obter uma paleta.) seu aplicativo pode obter a paleta enviando a mensagem [**ICM \_ descompactar \_ obter a \_ paleta**](icm-decompress-get-palette.md) (ou usar a macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) ).

## <a name="decompressor-initialization"></a>Inicialização do descompactador

Depois que o aplicativo selecionar um descompactador que possa manipular os formatos de entrada e saída de que precisa, você poderá inicializar o descompactador usando a função [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) . Essa função requer o identificador do descompactador e os formatos de entrada e saída.

## <a name="data-decompression"></a>Descompactação de dados

Você pode usar a função [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) para descompactar um quadro. Seu aplicativo deve usar essa função repetidamente até que todos os quadros em uma sequência sejam descompactados.

Se o fluxo de vídeo estiver atrasado atrás de outros componentes (como áudio) durante a reprodução, o aplicativo poderá especificar o sinalizador **ICDECOMPRESS \_ HURRYUP** para acelerar a descompactação. Para fazer isso, um descompactador pode extrair apenas as informações necessárias para descompactar o próximo quadro e não descompactar completamente o quadro atual. Portanto, seu aplicativo não deve tentar desenhar os dados descompactados quando ele usar esse sinalizador.

depois que o aplicativo tiver descompactado os dados, ele poderá enviar a mensagem de [**\_ \_ final ICM DECOMPRESSEX**](icm-decompressex-end.md) (ou usar a macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) ) para notificar o descompactador de que ele foi concluído. Se você quiser reiniciar a descompactação depois de usar essa função, seu aplicativo deverá reinicializar o descompactador usando [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços VCMs](vcm-services.md)
</dt> </dl>

 

 