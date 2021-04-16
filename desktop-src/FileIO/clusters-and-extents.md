---
description: 'Os clusters podem ser referidos de duas perspectivas diferentes: dentro do arquivo e no volume.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Clusters e extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761737"
---
# <a name="clusters-and-extents"></a>Clusters e extensões

Os clusters podem ser referidos de duas perspectivas diferentes: dentro do arquivo e no volume. Qualquer cluster em um arquivo tem um VCN ( *número de cluster virtual* ), que é seu deslocamento relativo desde o início do arquivo. Por exemplo, uma busca duas vezes o tamanho de um cluster, seguido por uma leitura, retornará dados que começam no terceiro VCN. Um LCN ( *número de cluster lógico* ) descreve o deslocamento de um cluster de um ponto arbitrário dentro do volume. LCNs deve ser tratado somente como números ordinais ou relativos. Não há nenhum mapeamento garantido de clusters lógicos para setores de unidade de disco rígido físico.

Uma *extensão* é uma execução de clusters contíguos. Por exemplo, suponha que um arquivo que consiste em 30 clusters seja gravado em duas extensões. A primeira extensão pode consistir em cinco clusters contíguos, o outro dos 25 clusters restantes.

Não há nenhuma garantia de nenhuma relação no disco de qualquer extensão para qualquer outra extensão. Por exemplo, a primeira extensão pode estar em um LCN maior do que uma extensão subsequente.

 

 



