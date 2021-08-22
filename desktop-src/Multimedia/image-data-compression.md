---
title: Image-Data compactação
description: Image-Data compactação
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- VCM (gerenciador de compactação de vídeo), compactação de dados de imagem
- VCM (gerenciador de compactação de vídeo), compactação de dados de imagem
- Função ICCompress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf638467e3685b24a65cd47492faed6660e77e5c49864a339a3874eb81e9b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038676"
---
# <a name="image-data-compression"></a>Image-Data compactação

Seu aplicativo pode usar uma série de funções e macros [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) para compactar dados. As funções e macros podem ajudá-lo a executar as seguintes tarefas:

-   Determine o formato de compactação a ser usado para um formato de entrada especificado.
-   Prepare o sr.
-   Compactar os dados.
-   Encerrar a compactação.

Seu aplicativo pode aumentar o controle sobre o processo de compactação usando as funções e macros [**ICCompress.**](/windows/desktop/api/Vfw/nf-vfw-iccompress) Esse grupo de funções e macros lida com quadros individuais, em vez da sequência como um todo. Por exemplo, seu aplicativo pode identificar os quadros a compactar como quadros-chave usando a **função ICCompress.**

Um feirante recebe dados em um formato, compacta os dados e retorna uma versão compactada dos dados usando um formato especificado. O formato de entrada típico especifica DIBs usando a [**estrutura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) O formato de saída típico especifica DIBs compactados, também usando a **estrutura BITMAPINFO.**

> [!Note]  
> Para minimizar a degradação de imagem e áudio durante a reprodução, evite compactar um arquivo AVI mais de uma vez. Combine partes de vídeo descompactadas em seu sistema de edição e, em seguida, compacte o produto final.

 

## <a name="compressor-and-compression-format-selection"></a>Seleção de formato de compactação e Depress

Se você quiser compactar dados e seu aplicativo exigir um formato de saída específico, envie a mensagem [**\_ COMPRESS \_ QUERY**](icm-compress-query.md) do ICM (ou use a macro [**ICCompressQuery)**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) para consultar o grupo para determinar se ele dá suporte aos formatos de entrada e saída.

Se o formato de saída não for importante para seu aplicativo, você só precisará encontrar um que possa manipular o formato de entrada. Para determinar se um ltda pode manipular o formato de entrada, você pode enviar ICM **\_ \_ CONSULTA COMPRESS**, especificando **NULL** para o *parâmetro lParam.* Essa mensagem não retorna o formato de saída para seu aplicativo. Seu aplicativo pode determinar o tamanho do buffer necessário para os dados que especificam o formato de compactação enviando a mensagem [**\_ ICM COMPRESS GET \_ \_ FORMAT**](icm-compress-get-format.md) (ou use a macro [**ICCompressGetFormatSize).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) Você também pode recuperar os dados de formato enviando ICM \_ \_ COMPRESS GET \_ FORMAT (ou a macro [**ICCompressGetFormat).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat)

Se você quiser determinar o maior buffer que o widget pode exigir para compactação, envie a mensagem [**\_ ICM COMPRESS GET \_ \_ SIZE**](icm-compress-get-size.md) (ou use a macro [**ICCompressGetSize).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) Você pode usar o número de bytes retornados pela [**função ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) para alocar um buffer para compactações de imagem subsequentes.

## <a name="compressor-initialization"></a>Inicialização de Ltda

Depois que seu aplicativo selecionar um grupo que possa lidar com os formatos de entrada e saída necessários, você poderá inicializar o grupo usando a mensagem [**BEGIN ICM \_ \_ COMPRESS**](icm-compress-begin.md) (ou usar a macro [**ICCompressBegin).**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) Essa mensagem requer o handle de ltda e os formatos de entrada e saída.

## <a name="data-compression"></a>Data Compression

Você pode usar a [**função ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) para compactar um quadro. Seu aplicativo deve usar essa função repetidamente até que todos os quadros em uma sequência sejam compactados. Seu aplicativo também deve acompanhar e incrementar o número de cada quadro compactado com **ICCompress**. O jogador usa esse valor para verificar se os quadros são enviados fora de ordem durante a compactação temporal rápida (armazenar diferenças entre quadros sucessivos). Se o aplicativo recompactar um quadro, ele deverá usar o mesmo número de quadro de quando o quadro foi compactado pela primeira vez. Se o aplicativo compactar uma imagem de quadro ainda, ele poderá especificar um número de quadro de zero.

Seu aplicativo pode usar o **sinalizador ICCOMPRESS \_ KEYFRAME** para tornar o quadro compactado pelo [**ICCompress um**](/windows/desktop/api/Vfw/nf-vfw-iccompress) quadro-chave.

Quando o VCM retorna o controle para seu aplicativo depois de compactar um quadro, o VCM armazena os dados compactados nas estruturas referenciadas pelos *parâmetros lpbiOutput* e *lpData.* Se o aplicativo precisar mover os dados compactados, ele poderá encontrar seu tamanho no membro *biSizeImage* da estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) especificada em *lpbiOutput.*

> [!Note]  
> Seu aplicativo deve alocar as estruturas e buffers que armazenam os dados descompactados e compactados. Se o for compatível com a compactação temporal, seu aplicativo também deverá alocar uma estrutura e um buffer para manter o formato e os dados do quadro anterior de informações.

 

## <a name="ending-compression"></a>Terminando a compactação

Depois que o aplicativo compactar os dados, ele poderá usar a macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) para notificar o solicitante de que ele foi concluído. Se você quiser reiniciar a compactação depois de usar essa função, seu aplicativo deverá reinicializar o widget enviando a mensagem BEGIN ICM [**\_ COMPRESS \_**](icm-compress-begin.md) (ou use a macro [**ICCompressBegin).**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin)

 

 