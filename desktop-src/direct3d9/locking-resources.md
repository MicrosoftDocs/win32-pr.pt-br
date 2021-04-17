---
description: Bloquear um recurso significa conceder acesso de CPU ao seu armazenamento.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Recursos de bloqueio (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105782694"
---
# <a name="locking-resources-direct3d-9"></a>Recursos de bloqueio (Direct3D 9)

Bloquear um recurso significa conceder acesso de CPU ao seu armazenamento. As seguintes opções de bloqueio são definidas para recursos:

-   \_Descartar D3DLOCK
-   D3DLOCK \_ ReadOnly
-   D3DLOCK \_ NOoverwrite
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ nenhuma \_ \_ atualização suja

Para obter detalhes sobre sinalizadores de bloqueio e como eles se relacionam com recursos específicos, consulte as páginas de referência nos métodos de bloqueio de recursos individuais. Os desenvolvedores de aplicativos devem observar que os \_ sinalizadores D3DLOCK descartar, D3DLOCK \_ ReadOnly e D3DLOCK \_ NoOverwrite são apenas dicas. O tempo de execução não verifica se os aplicativos estão seguindo a funcionalidade especificada por esses sinalizadores. Um aplicativo que especifica D3DLOCK \_ ReadOnly, mas, em seguida, grava no recurso deve esperar resultados indefinidos. Em geral, o trabalho contra sinalizadores de bloqueio, incluindo os sinalizadores de uso de bloqueio, não tem garantia de trabalho em versões posteriores e pode incorrer em uma penalidade de desempenho significativa.

Uma operação de bloqueio é seguida por uma operação de desbloqueio. Por exemplo, depois de bloquear uma textura, o aplicativo, subsequentemente, cede o acesso direto a texturas bloqueadas desbloqueando-as. Além de conceder acesso ao processador, qualquer outra operação que envolva esse recurso será serializada durante um bloqueio. Apenas um único bloqueio para um recurso é permitido, mesmo para regiões não sobrepostas, e nenhuma operação de aceleração em uma superfície pode ser contínua enquanto uma Operation de bloqueio está pendente nessa superfície.

Cada interface de recurso tem métodos para bloquear os buffers contidos. Cada recurso de textura também pode bloquear uma subparte desse recurso. os recursos 2D (superfícies) permitem o bloqueio de subretângulos e os recursos de volume permitem o bloqueio de subvolumes ou caixas. Cada método de bloqueio retorna uma estrutura que contém um ponteiro para o armazenamento que faz o backup do recurso e os valores que representam as distâncias entre linhas ou planos de dados, dependendo do tipo de recurso. Para obter detalhes, consulte as listas de métodos para as interfaces de recurso. O ponteiro retornado sempre aponta para o byte superior esquerdo nas subregiãos bloqueadas.

Ao trabalhar com buffers de índice e vértice, você pode fazer várias chamadas de bloqueio; no entanto, você deve garantir que o número de chamadas de bloqueio corresponda ao número de chamadas de desbloqueio.

O DXTn armazena pixels em blocos 4x4 codificados e só pode ser bloqueado em limites de 4x4.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



