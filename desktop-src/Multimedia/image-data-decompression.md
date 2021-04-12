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
ms.openlocfilehash: 25614f157436056f7f24c340f6cc6f4dbc62d9ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293971"
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

Se o formato de saída não for importante em seu aplicativo, você precisará localizar apenas um descompactador que possa manipular o formato de entrada. Para determinar se um descompactador pode manipular o formato de entrada, use [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) e especifique **NULL** para o parâmetro *lpbiDst* . Seu aplicativo pode determinar o tamanho do buffer necessário para os dados que especificam o formato de descompactação enviando a mensagem [**ICM \_ descompactar \_ Get \_ Format**](icm-decompress-get-format.md) (ou usar a macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) ). Você também pode enviar **o \_ formato de \_ Get \_ do ICM** (ou a macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) ) para recuperar os dados de formato. O descompactador retorna seu formato sugerido em uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Esse formato normalmente preserva a maioria das informações durante a descompactação. Seu aplicativo deve garantir que o descompactador retorne com êxito antes de descompactar as informações.

Como seu aplicativo aloca a memória necessária para descompactação, ele precisa determinar a memória máxima que o descompactador pode exigir para o formato de saída. A mensagem de **\_ \_ obter \_ formato do ICM descompactar** Obtém o número de bytes que o descompactador usa para o formato padrão.

Se seu aplicativo define seu próprio formato usando [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery), ele também deve obter uma paleta para o bitmap; **ICDecompressExQuery** não fornece definições de paleta. (A maioria dos aplicativos usa formatos padrão e não precisa obter uma paleta.) Seu aplicativo pode obter a paleta enviando a mensagem [**ICM \_ descompactar a \_ \_ paleta**](icm-decompress-get-palette.md) (ou usar a macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) ).

## <a name="decompressor-initialization"></a>Inicialização do descompactador

Depois que o aplicativo selecionar um descompactador que possa manipular os formatos de entrada e saída de que precisa, você poderá inicializar o descompactador usando a função [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) . Essa função requer o identificador do descompactador e os formatos de entrada e saída.

## <a name="data-decompression"></a>Descompactação de dados

Você pode usar a função [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) para descompactar um quadro. Seu aplicativo deve usar essa função repetidamente até que todos os quadros em uma sequência sejam descompactados.

Se o fluxo de vídeo estiver atrasado atrás de outros componentes (como áudio) durante a reprodução, o aplicativo poderá especificar o sinalizador **ICDECOMPRESS \_ HURRYUP** para acelerar a descompactação. Para fazer isso, um descompactador pode extrair apenas as informações necessárias para descompactar o próximo quadro e não descompactar completamente o quadro atual. Portanto, seu aplicativo não deve tentar desenhar os dados descompactados quando ele usar esse sinalizador.

Depois que o aplicativo tiver descompactado os dados, ele poderá enviar a mensagem de [**\_ \_ final DECOMPRESSEX do ICM**](icm-decompressex-end.md) (ou usar a macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) ) para notificar o descompactador de que ele foi concluído. Se você quiser reiniciar a descompactação depois de usar essa função, seu aplicativo deverá reinicializar o descompactador usando [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços VCMs](vcm-services.md)
</dt> </dl>

 

 