---
description: Bloquear um recurso significa conceder acesso de CPU ao seu armazenamento.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Recursos de bloqueio (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6cdb7cde646bd5073bc0c5b574694be69f05f1bf15d8c5c08e00b7182cfe044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799489"
---
# <a name="locking-resources-direct3d-9"></a>Recursos de bloqueio (Direct3D 9)

Bloquear um recurso significa conceder acesso de CPU ao seu armazenamento. As seguintes opções de bloqueio são definidas para recursos:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ SEM \_ ATUALIZAÇÃO \_ SUJA

Para obter detalhes sobre sinalizadores de bloqueio e como eles se relacionam com recursos específicos, consulte as páginas de referência nos métodos de bloqueio de recursos individuais. Os desenvolvedores de aplicativos devem observar que os sinalizadores \_ D3DLOCK DISCARD, D3DLOCK \_ READONLY e D3DLOCK \_ NOOVERWRITE são apenas dicas. O tempo de executar não verifica se os aplicativos estão seguindo a funcionalidade especificada por esses sinalizadores. Um aplicativo que especifica D3DLOCK READONLY, mas, em seguida, grava no recurso deve \_ esperar resultados indefinido. Em geral, trabalhar contra sinalizadores de bloqueio, incluindo os sinalizadores de uso de bloqueio, não tem garantia de funcionar em versões posteriores e pode incorrer em uma penalidade de desempenho significativa.

Uma operação de bloqueio é seguida por uma operação de desbloqueio. Por exemplo, depois de bloquear uma textura, o aplicativo subsequentemente abre mão do acesso direto a texturas bloqueadas desbloqueando-as. Além de conceder acesso ao processador, todas as outras operações que envolvem esse recurso são serializadas durante um bloqueio. Somente um único bloqueio para um recurso é permitido, mesmo para regiões não sobrepostas, e nenhuma operação de acelerador em uma superfície pode estar em andamento enquanto uma operação de bloqueio é pendente nessa superfície.

Cada interface de recurso tem métodos para bloquear os buffers contidos. Cada recurso de textura também pode bloquear uma sub porção desse recurso. Recursos 2D (superfícies) permitem o bloqueio de sub retângulos e os recursos de volume permitem o bloqueio de sub volumes ou caixas. Cada método de bloqueio retorna uma estrutura que contém um ponteiro para o armazenamento que dá apoio ao recurso e valores que representam as distâncias entre linhas ou planos de dados, dependendo do tipo de recurso. Para obter detalhes, consulte as listas de métodos para as interfaces de recurso. O ponteiro retornado sempre aponta para o byte superior esquerdo nas sub-regiões bloqueadas.

Ao trabalhar com buffers de índice e vértice, você pode fazer várias chamadas de bloqueio; No entanto, você deve garantir que o número de chamadas de bloqueio corresponde ao número de chamadas de desbloqueio.

O DXTn armazena pixels em blocos codificados 4x4 e só pode ser bloqueado em limites 4x4.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



