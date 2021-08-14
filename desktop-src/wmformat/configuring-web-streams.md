---
title: configurando Fluxos Web
description: configurando Fluxos Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- fluxos, configurando fluxos da Web
- codecs, configurando fluxos da Web
- Fluxos da Web, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8df1ced96a772a26b674fb47a30a8664d6431ff946328f45467554857b1ee4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199117"
---
# <a name="configuring-web-streams"></a>configurando Fluxos Web

Os fluxos da Web são um tipo especializado de fluxo de transferência de arquivos usado para entregar os arquivos associados a um site em um único fluxo. A configuração de fluxo da Web está resumida na tabela a seguir.



| Configuração                                            | Descrição                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **Tipo de mídia do WM \_ \_ . majortype**                      | Defina como WMMEDIATYPE \_ FileTransfer.                                                 |
| **Tipo de mídia do WM \_ \_ . subtipo**                        | Defina como \_ webstream do WMMEDIASUBTYPE.                                                 |
| **Tipo de mídia do WM \_ \_ . bFixedSizeSamples**              | Defina como false.                                                                     |
| **Tipo de mídia do WM \_ \_ . bTemporalCompression**           | Defina como true.                                                                      |
| **Tipo de mídia do WM \_ \_ . lSampleSize**                    | Defina como 0.                                                                         |
| **Tipo de mídia do WM \_ \_ . FormatType**                     | Defina como \_ webstream do WMFORMAT.                                                       |
| **Tipo de mídia do WM \_ \_ . punk**                           | Defina como **nulo**.                                                                  |
| **Tipo de mídia do WM \_ \_ . cbFormat**                       | Defina como `sizeof(WMT_WEBSTREAM_FORMAT)`.                                            |
| **Tipo de mídia do WM \_ \_ . pbFormat**                       | Defina como o endereço de uma estrutura de **\_ \_ formato de webstream do WMT** corretamente configurada. |
| **\_Formato WEBstream do WMT \_ . cbSampleHeaderFixedData** | Defina como `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.                                     |
| **\_Formato WEBstream do WMT \_ . wVersion**                | defina como 1.                                                                         |
| **\_Formato WEBstream do WMT \_ . wReserved**               | Defina como 0.                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configuração comum a todos os Fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Fluxos Web**](web-streams.md)
</dt> </dl>

 

 




