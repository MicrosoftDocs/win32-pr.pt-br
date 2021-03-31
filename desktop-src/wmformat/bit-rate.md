---
title: Taxa de bits
description: Taxa de bits
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- SDK do Windows Media Format, taxas de bits
- ASF (Advanced Systems Format), taxas de bits
- ASF (formato de sistemas avançados), taxas de bits
- taxas de bits, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636972"
---
# <a name="bit-rate"></a>Taxa de bits

Taxa de bits refere-se à quantidade de dados por segundo que é entregue de um arquivo ASF. As medições de taxa de bits são em bits por segundo (bps) ou kilobits por segundo (Kbps). A taxa de bits geralmente é confundida com largura de banda, que é uma medida da capacidade de transferência de dados de uma rede. A largura de banda também é medida em bps e kbps.

O Windows Media Format SDK pode ser usado para criar aplicativos que fornecem fluxo de conteúdo baseado no Windows Media por meio de locais da Internet ou da intranet. Quando você está transmitindo dados por uma rede ou pela Internet, a taxa de bits é de importância vital para a experiência do usuário final. Se a largura de banda disponível para a rede for menor que a taxa de bits do arquivo ASF, a reprodução do arquivo será interrompida de alguma forma. Normalmente, a largura de banda insuficiente fará com que os exemplos sejam ignorados ou uma pausa na reprodução enquanto mais dados são armazenados em buffer.

Cada arquivo ASF recebe um valor de taxa de bits no momento da criação, com base no tipo e no número de fluxos incluídos no perfil usado. Os fluxos individuais têm suas próprias taxas de bits. As taxas de bits podem ser constantes (os dados originais são compactados de forma a manter um fluxo constante de dados em aproximadamente a mesma taxa) ou variável (os dados originais são compactados de forma a manter a mesma qualidade em todo o tempo, mesmo que isso possa significar um fluxo de dados irregular). Tipos de taxa de bits diferentes podem ser aplicados a fluxos diferentes no mesmo arquivo.

Você pode codificar o mesmo conteúdo para vários fluxos diferentes, cada um com uma taxa de bits diferente. Em seguida, você pode configurar os fluxos para que eles sejam mutuamente exclusivos. Isso permite que você crie um único arquivo que pode ser transmitido para usuários com larguras de banda diferentes. Esse recurso é chamado de taxa de bits múltipla ou MBR.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Codificação de taxa de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Entradas, fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Perfis**](profiles.md)
</dt> <dt>

[**Codificação de taxa de bits variável (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




