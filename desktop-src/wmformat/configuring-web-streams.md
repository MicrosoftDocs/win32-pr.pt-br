---
title: Configurando fluxos da Web
description: Configurando fluxos da Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- fluxos, configurando fluxos da Web
- codecs, configurando fluxos da Web
- Fluxos da Web, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292675"
---
# <a name="configuring-web-streams"></a>Configurando fluxos da Web

Os fluxos da Web são um tipo especializado de fluxo de transferência de arquivos usado para entregar os arquivos associados a um site em um único fluxo. A configuração de fluxo da Web está resumida na tabela a seguir.



| Configuração                                            | Descrição                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **Tipo de mídia do WM \_ \_ . majortype**                      | Defina como WMMEDIATYPE \_ FileTransfer.                                                 |
| **Tipo de mídia do WM \_ \_ . subtipo**                        | Defina como \_ webstream do WMMEDIASUBTYPE.                                                 |
| **Tipo de mídia do WM \_ \_ . bFixedSizeSamples**              | Defina como false.                                                                     |
| **Tipo de mídia do WM \_ \_ . bTemporalCompression**           | Defina como True.                                                                      |
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

[**Configuração comum a todos os fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Fluxos da Web**](web-streams.md)
</dt> </dl>

 

 




