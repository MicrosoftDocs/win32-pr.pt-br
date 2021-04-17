---
title: Compactação de Image-Data
description: Compactação de Image-Data
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- VCM (Gerenciador de compactação de vídeo), compactação de dados de imagem
- VCM (Gerenciador de compactação de vídeo), compactação de dados de imagem
- Função ICCompress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8f59a163a9b5a74d2d2fe984417069985fa86a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365896"
---
# <a name="image-data-compression"></a>Compactação de Image-Data

Seu aplicativo pode usar uma série de funções e macros [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) para compactar dados. As funções e macros podem ajudá-lo a executar as seguintes tarefas:

-   Determine o formato de compactação a ser usado para um formato de entrada especificado.
-   Prepare o compressor.
-   Compacte os dados.
-   Encerrar compactação.

Seu aplicativo pode aumentar o controle sobre o processo de compactação usando as funções e macros [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) . Esse grupo de funções e macros manipula quadros individuais, em vez da sequência como um todo. Por exemplo, seu aplicativo pode identificar os quadros a serem compactados como quadros-chave usando a função **ICCompress** .

Um compressor recebe dados em um formato, compacta os dados e retorna uma versão compactada dos dados usando um formato especificado. O formato de entrada típico especifica DIBs usando a estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . O formato de saída típico especifica DIBs comprimido, também usando a estrutura **BITMAPINFO** .

> [!Note]  
> Para minimizar a degradação da imagem e do áudio durante a reprodução, evite compactar um arquivo AVI mais de uma vez. Combine pedaços de vídeo não compactados em seu sistema de edição e, em seguida, compacte o produto final.

 

## <a name="compressor-and-compression-format-selection"></a>Seleção de formato de compactador e compactação

Se você quiser compactar dados e seu aplicativo exigir um formato de saída específico, envie a mensagem de [**\_ \_ consulta de compactação ICM**](icm-compress-query.md) (ou use a macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) ) para consultar o compressor para determinar se ele dá suporte aos formatos de entrada e saída.

Se o formato de saída não for importante para seu aplicativo, você só precisa encontrar um compressor que possa manipular o formato de entrada. Para determinar se um compressor pode manipular o formato de entrada, você pode enviar a **\_ \_ consulta de compactação ICM**, especificando **NULL** para o parâmetro *lParam* . Essa mensagem não retorna o formato de saída para seu aplicativo. Seu aplicativo pode determinar o tamanho do buffer necessário para os dados que especificam o formato de compactação enviando a mensagem [**ICM \_ Compact \_ Get \_ Format**](icm-compress-get-format.md) (ou use a macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) ). Você também pode recuperar os dados de formato enviando o \_ \_ formato de Get compactar ICM \_ (ou a macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) ).

Se você quiser determinar o buffer maior que o compressor poderia exigir para compactação, envie a mensagem [**ICM \_ Compact \_ Get \_ size**](icm-compress-get-size.md) (ou use a macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) ). Você pode usar o número de bytes retornados pela função [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) para alocar um buffer para as compactações de imagem subsequentes.

## <a name="compressor-initialization"></a>Inicialização de compactador

Depois que o aplicativo selecionar um compressor que possa lidar com os formatos de entrada e saída de que precisa, você poderá inicializar o compactador usando a mensagem de [**\_ \_ início de compactação ICM**](icm-compress-begin.md) (ou use a macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) ). Essa mensagem requer o identificador de compressor e os formatos de entrada e saída.

## <a name="data-compression"></a>Data Compression

Você pode usar a função [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) para compactar um quadro. Seu aplicativo deve usar essa função repetidamente até que todos os quadros em uma sequência sejam compactados. Seu aplicativo também deve acompanhar e incrementar o número de cada quadro compactado com **ICCompress**. O compressor usa esse valor para verificar se os quadros são enviados fora de ordem durante a compactação temporal rápida (armazenando diferenças entre quadros sucessivos). Se o seu aplicativo recompactar um quadro, ele deverá usar o mesmo número de quadro que quando o quadro foi compactado pela primeira vez. Se seu aplicativo compacta uma imagem de quadro ainda, ele pode especificar um número de quadro igual a zero.

Seu aplicativo pode usar o sinalizador **ICCOMPRESS \_ KEYFRAME** para tornar o quadro compactado por [**ICCOMPRESS**](/windows/desktop/api/Vfw/nf-vfw-iccompress) um quadro-chave.

Quando VCM retorna o controle ao seu aplicativo depois de compactar um quadro, o VCM armazena os dados compactados nas estruturas referenciadas pelos parâmetros *lpbiOutput* e *lpData* . Se seu aplicativo precisar mover os dados compactados, ele poderá encontrar seu tamanho no membro *biSizeImage* da estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) especificada em *lpbiOutput*.

> [!Note]  
> Seu aplicativo deve alocar as estruturas e os buffers que armazenam os dados descompactados e compactados. Se o compressor oferecer suporte à compactação temporal, o aplicativo também deverá alocar uma estrutura e um buffer para manter o formato e os dados do quadro de informações anterior.

 

## <a name="ending-compression"></a>Finalizando compactação

Depois que o aplicativo tiver compactado os dados, ele poderá usar a macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) para notificar o compressor de que ele foi concluído. Se você quiser reiniciar a compactação depois de usar essa função, seu aplicativo deverá reinicializar o compactador enviando a mensagem de [**início do ICM \_ compactar \_**](icm-compress-begin.md) (ou usar a macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) ).

 

 