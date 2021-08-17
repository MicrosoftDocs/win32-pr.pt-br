---
title: Convertendo dados de um formato para outro
description: Convertendo dados de um formato para outro
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Gerenciador de compactação de áudio (ACM), convertendo dados
- ACM (Gerenciador de compactação de áudio), convertendo dados
- Exemplos do ACM, convertendo dados
- convertendo dados
- função acmStreamOpen
- função acmStreamSize
- função acmStreamPrepareHeader
- função acmStreamConvert
- função acmStreamUnprepareHeader
- função acmStreamClose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ec1050066b92a356067085b491f5ddbf4bded47789c6e15a5187ea74c47c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144800"
---
# <a name="converting-data-from-one-format-to-another"></a>Convertendo dados de um formato para outro

O ACM usa funções de fluxo para dar suporte à conversão de formato de dados. Os conversores no ACM alteram o formato, mas não o tipo de dados. Por exemplo, um módulo conversor pode alterar 44-kHz, dados de 16 bits para 44-kHz, dados de 8 bits.

As seguintes funções do ACM dão suporte à conversão de formato de dados. Eles são listados na ordem em que você normalmente os usaria.

-   A função [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) abre um fluxo de conversão.
-   A função [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcula o tamanho apropriado do buffer de origem ou de destino.
-   A função [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prepara os buffers de origem e de destino a serem usados em uma conversão.
-   A função [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) converte dados em um buffer de origem no formato de destino, gravando os dados convertidos no buffer de destino.
-   A função [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) limpa os buffers de origem e de destino preparados pelo **acmStreamPrepareHeader**. Você deve chamar essa função antes de liberar os buffers de origem e de destino.
-   A função [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) fecha um fluxo de conversão.

Ao converter dados, primeiro identifique o formato de origem e, em seguida, escolha o formato de destino. A maneira mais fácil de fazer isso é usando a função [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , que exibe uma caixa de diálogo de seleção de formato e retorna a opção de formato do usuário.

Quando você conhece os formatos de origem e destino, pode usar [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) para abrir um fluxo de conversão. Em seguida, você pode usar a função [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) para determinar os tamanhos de buffer apropriados.

A próxima etapa é preparar os buffers a serem usados na conversão usando [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).

Para executar a conversão, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) até que todos os buffers tenham sido processados. Quando a conversão for concluída, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) para limpar os buffers e, em seguida, use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) para fechar o fluxo de conversão.

 

 




