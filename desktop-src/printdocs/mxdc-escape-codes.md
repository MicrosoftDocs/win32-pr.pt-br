---
description: Esta seção descreve as estruturas que são usadas com a \_ função de escape MXDC e o conversor de documento XPS da Microsoft (MXDC).
ms.assetid: 102dc056-7f65-47d4-8bcd-3b11608bdb9c
title: Estruturas de código de escape MXDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b35c393d00dab227a91cbbb55eeca62039b41ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797544"
---
# <a name="mxdc-escape-code-structures"></a>Estruturas de código de escape MXDC

Esta seção descreve as estruturas que são usadas com a função de [**\_ escape MXDC**](mxdc-escape.md) e o conversor de documento XPS da Microsoft (MXDC).

## <a name="in-this-section"></a>Nesta seção



| Estrutura                                                                              | Descrição                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_cabeçalho de escape MXDC \_ \_ T**](mxdcescapeheader.md)<br/>                         | A [**estrutura \_ \_ \_ T do cabeçalho de escape MXDC**](/windows/desktop/printdocs/mxdcescapeheader) contém o código da operação para uma chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com [**MXDC \_ escape**](mxdc-escape.md) como o parâmetro *nEscape* . Ele também fornece os tamanhos dos buffers de entrada e saída.<br/>  |
| [**MXDC \_ obter \_ dados de nome de arquivo \_ \_ T**](mxdcgetfilenamedata.md)<br/>                 | A estrutura [**MXDC \_ Get \_ filename \_ Data \_ T**](/windows/desktop/printdocs/mxdcgetfilenamedata) contém o caminho completo e o nome do arquivo de um arquivo de saída do conversor de documento XPS da Microsoft (MXDC).<br/>                                                                                                     |
| [**ESCAPE de MXDC \_ PRINTTICKET \_ \_**](mxdcprintticketescape.md)<br/>               | A [**estrutura \_ \_ \_ t de escape do MXDC PRINTTICKET**](mxdcprintticketescape.md) é uma estrutura [**\_ \_ \_ t do cabeçalho de escape do MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ dados \_ t do MXDC PRINTTICKET**](mxdcprintticketpassthrough.md) .<br/>                            |
| [**\_ \_ Data \_ T do MXDC PRINTTICKET**](mxdcprintticketpassthrough.md)<br/>            | A estrutura de [**\_ \_ dados \_ T do MXDC PRINTTICKET**](/windows/desktop/printdocs/mxdcprintticketpassthrough) contém um TÍQUETE de impressão de documento XPS, que contém configurações de impressora e trabalho de impressão, para passar para o arquivo de saída do conversor de documento XPS da Microsoft (MXDC) sem nenhum processamento.<br/>              |
| [**MXDC \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md)<br/>                             | A estrutura de [**\_ T de \_ dados \_ MXDC S0PAGE**](/windows/desktop/printdocs/mxdcs0pagedata) contém uma página de documento XPS a ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC) sem nenhum processamento.<br/>                                                                                  |
| [**MXDC \_ S0PAGE \_ PassThrough \_ escape \_ T**](mxdcs0pagepassthroughescape.md)<br/> | A [**estrutura \_ \_ t de \_ escape \_ de passagem MXDC S0PAGE**](/windows/desktop/printdocs/mxdcs0pagepassthroughescape) é uma estrutura [**\_ \_ \_ t de cabeçalho de escape MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ f Data \_ T MXDC S0PAGE**](mxdcs0pagedata.md) .<br/>                             |
| [**MXDC \_ S0PAGE \_ de \_ escape de recurso \_**](mxdcs0pageresourceescape.md)<br/>       | A [**estrutura \_ \_ t de \_ escape \_ de recursos do MXDC S0PAGE**](/windows/desktop/printdocs/mxdcs0pageresourceescape) é uma estrutura [**\_ \_ \_ t de cabeçalho de escape MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ \_ f Resource \_ T MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .<br/>                   |
| [**MXDC \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md)<br/>             | A [**estrutura \_ \_ T do \_ recurso \_ MXDC XPS S0PAGE**](/windows/desktop/printdocs/mxdcxpss0pageresource) contém informações sobre um recurso, como uma imagem ou uma fonte, que está associada a uma página de documento XPS e que deve ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC).<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MXDC \_ escape**](mxdc-escape.md)
</dt> </dl>

 

