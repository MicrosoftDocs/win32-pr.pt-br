---
description: Esta seção descreve as estruturas usadas com a função MXDC ESCAPE e o MXDC (Conversor de Documentos do \_ Microsoft XPS).
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: Estruturas de código de escape MXDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b87ef962be9f8fffa1ae0b2d126cecfda4cc157118f4defd21360b030dc9d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948386"
---
# <a name="mxdc-escape-code-structures"></a>Estruturas de código de escape MXDC

Esta seção descreve as estruturas usadas com a [**função \_ MXDC ESCAPE**](mxdc-escape.md) e o MXDC (Conversor de Documentos do Microsoft XPS).

## <a name="in-this-section"></a>Nesta seção



| Estrutura                                                                              | Descrição                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HEADER DE ESCAPE DO MXDC \_ \_ \_ T**](mxdcescapeheader.md)<br/>                         | A [**estrutura T do MXDC ESCAPE \_ \_ \_ HEADER**](/windows/desktop/printdocs/mxdcescapeheader) contém o código de operação para uma chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com [**MXDC \_ ESCAPE**](mxdc-escape.md) como o *parâmetro nEscape.* Ele também fornece os tamanhos dos buffers de entrada e saída.<br/>  |
| [**MXDC \_ GET \_ FILENAME \_ DATA \_ T**](mxdcgetfilenamedata.md)<br/>                 | A [**estrutura MXDC \_ GET \_ FILENAME DATA \_ \_ T**](/windows/desktop/printdocs/mxdcgetfilenamedata) contém o caminho completo e o nome de arquivo de um arquivo de saída do MXDC (Conversor de Documentos) do Microsoft XPS.<br/>                                                                                                     |
| [**MXDC \_ PRINTTICKET \_ ESCAPE \_ T**](mxdcprintticketescape.md)<br/>               | A estrutura T do [**MXDC \_ PRINTTICKET \_ ESCAPE \_**](mxdcprintticketescape.md) é uma estrutura T do [**MXDC \_ ESCAPE \_ HEADER \_ concatenada**](mxdcescapeheader.md) com uma estrutura [**MXDC \_ PRINTTICKET \_ DATA \_ T.**](mxdcprintticketpassthrough.md)<br/>                            |
| [**MXDC \_ PRINTTICKET \_ DATA \_ T**](mxdcprintticketpassthrough.md)<br/>            | A estrutura [**MXDC \_ PRINTTICKET \_ DATA \_ T**](/windows/desktop/printdocs/mxdcprintticketpassthrough) contém um tíquete de impressão de documento XPS, que contém configurações de trabalho de impressão e impressora, para passar para o arquivo de saída do MXDC (Conversor de Documentos) do Microsoft XPS sem nenhum processamento.<br/>              |
| [**MXDC \_ S0PAGE \_ DATA \_ T**](mxdcs0pagedata.md)<br/>                             | A [**estrutura MXDC \_ S0PAGE \_ DATA \_ T**](/windows/desktop/printdocs/mxdcs0pagedata) contém uma página de documento XPS a ser passada para o arquivo de saída do MXDC (Conversor de Documentos) do Microsoft XPS sem nenhum processamento.<br/>                                                                                  |
| [**ESCAPE DE \_ PASSAGEM DE S0PAGE DO MXDC \_ \_ \_ T**](mxdcs0pagepassthroughescape.md)<br/> | A estrutura T de ESCAPE DE PASSAGEM [**\_ DE S0PAGE \_ \_ \_ do MXDC**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape) é uma estrutura T do [**\_ \_ HEADER \_ DE ESCAPE do MXDC**](mxdcescapeheader.md) concatenada com uma estrutura T de DADOS [**\_ S0PAGE \_ \_ do MXDC.**](mxdcs0pagedata.md)<br/>                             |
| [**MXDC \_ S0PAGE \_ RESOURCE \_ ESCAPE \_ T**](mxdcs0pageresourceescape.md)<br/>       | A estrutura T do [**MXDC \_ S0PAGE \_ RESOURCE \_ ESCAPE \_**](/windows/desktop/printdocs/mxdcs0pageresourceescape) é uma estrutura T do [**MXDC \_ ESCAPE \_ HEADER \_ concatenada**](mxdcescapeheader.md) com uma estrutura [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T.**](mxdcxpss0pageresource.md)<br/>                   |
| [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T**](mxdcxpss0pageresource.md)<br/>             | A estrutura [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T**](/windows/desktop/printdocs/mxdcxpss0pageresource) contém informações sobre um recurso, como uma imagem ou fonte, que está associada a uma página de documento XPS e deve ser passada para o arquivo de saída do MXDC (Conversor de Documentos) do Microsoft XPS.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

