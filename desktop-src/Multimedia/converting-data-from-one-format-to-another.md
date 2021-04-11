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
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292128"
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

 

 




