---
title: Taxa de bits
description: Taxa de bits
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows SDK de formato de mídia, taxas de bits
- ASF (Advanced Systems Format), taxas de bits
- ASF (formato de sistemas avançados), taxas de bits
- taxas de bits, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a15332e18d47a72974098ad38c6a942ceaf4780e1b79dffacd49382e3416ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809866"
---
# <a name="bit-rate"></a>Taxa de bits

Taxa de bits refere-se à quantidade de dados por segundo que é entregue de um arquivo ASF. As medições de taxa de bits são em bits por segundo (bps) ou kilobits por segundo (Kbps). A taxa de bits geralmente é confundida com largura de banda, que é uma medida da capacidade de transferência de dados de uma rede. A largura de banda também é medida em bps e kbps.

o SDK do formato de mídia Windows pode ser usado para criar aplicativos que fornecem streaming Windows conteúdo baseado em mídia de locais da Internet ou da intranet. Quando você está transmitindo dados por uma rede ou pela Internet, a taxa de bits é de importância vital para a experiência do usuário final. Se a largura de banda disponível para a rede for menor que a taxa de bits do arquivo ASF, a reprodução do arquivo será interrompida de alguma forma. Normalmente, a largura de banda insuficiente fará com que os exemplos sejam ignorados ou uma pausa na reprodução enquanto mais dados são armazenados em buffer.

Cada arquivo ASF recebe um valor de taxa de bits no momento da criação, com base no tipo e no número de fluxos incluídos no perfil usado. Os fluxos individuais têm suas próprias taxas de bits. As taxas de bits podem ser constantes (os dados originais são compactados de forma a manter um fluxo constante de dados em aproximadamente a mesma taxa) ou variável (os dados originais são compactados de forma a manter a mesma qualidade em todo o tempo, mesmo que isso possa significar um fluxo de dados irregular). Tipos de taxa de bits diferentes podem ser aplicados a fluxos diferentes no mesmo arquivo.

Você pode codificar o mesmo conteúdo para vários fluxos diferentes, cada um com uma taxa de bits diferente. Em seguida, você pode configurar os fluxos para que eles sejam mutuamente exclusivos. Isso permite que você crie um único arquivo que pode ser transmitido para usuários com larguras de banda diferentes. Esse recurso é chamado de taxa de bits múltipla ou MBR.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Codificação de taxa de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Perfis**](profiles.md)
</dt> <dt>

[**Codificação de taxa de bits variável (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




