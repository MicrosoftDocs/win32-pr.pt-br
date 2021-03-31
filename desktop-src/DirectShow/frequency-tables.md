---
description: Tabelas de frequência
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tabelas de frequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087286"
---
# <a name="frequency-tables"></a>Tabelas de frequência

O filtro de sintonizador de TV (kstvtune.ax) tem uma lista interna de tabelas de frequência. Cada tabela de frequência contém uma lista de frequências e corresponde à frequência de transmissão ou de cabo para um determinado país/região. Um aplicativo se ajusta a uma frequência específica chamando o método de [**\_ canal IAMTuner::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) com o índice da frequência desejada.

Para alguns países/regiões, os números de índice das tabelas de frequência são mapeados diretamente para números de canal. No entanto, os números de canal fixos não são apropriados para todos os mercados. Por exemplo, os números de canais europeus não são realmente usados pelos consumidores. Em vez disso, os consumidores esperam escolher e atribuir seus próprios números de canal para as frequências usadas pelos operadores de transmissão ou de cabo em sua área. Para esses países/regiões, os aplicativos não devem expor os números de índice diretamente para o usuário. Instread, o aplicativo deve manter um mapeamento interno entre os números de canal (apresentados ao usuário) e os índices de frequência (para ajuste).

A maioria dos operadores de cabo não-EUA está livre para transmitir frequências de sua escolha, muitas vezes misturando frequências de diferentes padrões na mesma lista de canais. Portanto, uma tabela de frequência "unicable" é usada para qualquer país/região que não possua uma autoridade de padrões de canal de cabo padrão. Além disso, um mecanismo é fornecido para substituir frequências individuais nas tabelas de frequência. Esse mecanismo é descrito na seção a seguir, [substituições de frequência](frequency-overrides.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ajuste de TV analógica internacional](international-analog-tv-tuning.md)
</dt> </dl>

 

 



