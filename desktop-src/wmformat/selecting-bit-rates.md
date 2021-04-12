---
title: Selecionando taxas de bits
description: Selecionando taxas de bits
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- perfis, escolhendo taxas de bits
- perfis, taxas de bits
- codecs, escolhendo taxas de bits
- codecs, taxas de bits
- perfis, selecionando taxas de bits
- codecs, selecionando taxas de bits
- taxas de bits, selecionando
- taxas de bits, perfis
- taxas de bits, codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291749"
---
# <a name="selecting-bit-rates"></a>Selecionando taxas de bits

Para arquivos que serão transmitidos em uma rede, você deve considerar cuidadosamente quais taxas de bits devem ser usadas. Na maioria das circunstâncias, você pode adicionar as taxas de bits de todos os fluxos em um arquivo em conjunto para obter uma ideia geral da largura de banda disponível necessária para transmitir o arquivo. No entanto, uma determinada quantidade de sobrecarga também é necessária para cada fluxo. Essa sobrecarga é resumida na tabela a seguir.



| Intervalo de taxa de bits (Kbps) | Largura de banda adicional necessária para sobrecarga (Kbps) |
|-----------------------|---------------------------------------------------|
| 10 a 16               | 3                                                 |
| 17 a 30               | 4                                                 |
| 31 a 45               | 5                                                 |
| 46 – 70               | 6                                                 |
| 71 – 225              | 7                                                 |
| >225               | 9                                                 |



 

A sobrecarga normal necessária para um fluxo não leva em conta as extensões de unidade de dados. Cada extensão de unidade de dados adiciona ao tamanho do exemplo ao qual está anexada. Dependendo do tipo de extensão de unidade de dados, isso pode aumentar muito a taxa de bits para o fluxo.

Você também deve considerar que a máxima largura de banda teórica disponível em uma conexão de rede não é uma taxa de bits de destino prática. A largura de banda média disponível para qualquer conexão fornecida é bem curta da capacidade de largura de banda da conexão, devido ao tráfego de rede e a muitos outros fatores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando perfis**](designing-profiles.md)
</dt> </dl>

 

 




