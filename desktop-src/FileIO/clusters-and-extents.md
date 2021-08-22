---
description: 'Os clusters podem ser referidos de duas perspectivas diferentes: dentro do arquivo e no volume.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Clusters e extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce987dc5c8afea842d6c92196474f88d17c36d2011995a2d760b83bfc1e5a644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533836"
---
# <a name="clusters-and-extents"></a>Clusters e extensões

Os clusters podem ser referidos de duas perspectivas diferentes: dentro do arquivo e no volume. Qualquer cluster em um arquivo tem um VCN ( *número de cluster virtual* ), que é seu deslocamento relativo desde o início do arquivo. Por exemplo, uma busca duas vezes o tamanho de um cluster, seguido por uma leitura, retornará dados que começam no terceiro VCN. Um LCN ( *número de cluster lógico* ) descreve o deslocamento de um cluster de um ponto arbitrário dentro do volume. LCNs deve ser tratado somente como números ordinais ou relativos. Não há nenhum mapeamento garantido de clusters lógicos para setores de unidade de disco rígido físico.

Uma *extensão* é uma execução de clusters contíguos. Por exemplo, suponha que um arquivo que consiste em 30 clusters seja gravado em duas extensões. A primeira extensão pode consistir em cinco clusters contíguos, o outro dos 25 clusters restantes.

Não há nenhuma garantia de nenhuma relação no disco de qualquer extensão para qualquer outra extensão. Por exemplo, a primeira extensão pode estar em um LCN maior do que uma extensão subsequente.

 

 



