---
title: Espaço de endereço disponível para recursos lado a lado
description: Esta seção especifica o espaço de endereço virtual disponível para recursos lado a lado.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5753fdb9d700689c6ebfffdae4368399c0e4bb36d328c9ff1a8cfc284005214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734278"
---
# <a name="address-space-available-for-tiled-resources"></a>Espaço de endereço disponível para recursos lado a lado

Esta seção especifica o espaço de endereço virtual disponível para recursos lado a lado.

Em sistemas operacionais de 64 bits, pelo menos 40 bits de espaço de endereço virtual (1 TB) está disponível.

Para sistemas operacionais de 32 bits, o espaço de endereço é de 32 bits (4 GB). Para sistemas ARM de 32 bits, a criação de recursos lado a lado individual poderá falhar se a alocação usar mais de 27 bits de espaço de endereço (128 MB). Isso inclui qualquer preenchimento oculto no espaço de endereço que do hardware pode usar para mipmaps, preenchimento de bloco empacotado e, possivelmente, preenchimento de dimensões de superfície para potências de 2.

Em sistemas de elementos gráficos com uma tabela de página separada para a unidade de processamento gráfico (GPU), a maior parte desse espaço de endereço estará disponível para os recursos GPU feitos pelo app, embora alocações de GPU feitas pelo driver de vídeo cabem no mesmo espaço.

Em sistemas futuros com uma tabela de página compartilhada entre a CPU e GPU, o espaço de endereço disponível é compartilhado entre todos os CPU e pela GPU alocações em um processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Parâmetros de criação de recursos lado a lado](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




