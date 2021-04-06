---
title: Características de desempenho
description: Uma chamada para a implementação do arquivo composto COM da Interface IPropertySetStorage para criar um conjunto de propriedades faz com que um fluxo ou um armazenamento seja criado por meio de uma chamada para o IStorage CreateStream ou IStorage CreateStorage.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8597862602a367ed93a3d6e5e0bcac76035c337a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917454"
---
# <a name="performance-characteristics"></a>Características de desempenho

Uma chamada para a implementação do arquivo composto COM da interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) para criar um conjunto de propriedades faz com que um fluxo ou um armazenamento seja criado por meio de uma chamada para [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ou [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage). Um conjunto de propriedades padrão é criado na memória, mas não é liberado para o disco. Quando há uma chamada para [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple), ela funciona dentro do buffer.

Quando um conjunto de propriedades é aberto, [IStorage:: OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [IStorage:: OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) é usado. O fluxo do conjunto de propriedades inteiro é lido na memória contígua. As operações [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) funcionam lendo o buffer de memória. Portanto, o primeiro acesso é caro em termos de tempo (devido a leituras de disco), mas os acessos subsequentes são muito eficientes. As gravações podem ser um pouco mais caras porque as operações SetSize no fluxo subjacente podem ser necessárias para garantir que o espaço em disco esteja disponível se os dados forem adicionados.

Nenhuma garantia é feita se [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) liberar as atualizações. Em geral, o cliente deve assumir que **IPropertyStorage:: WriteMultiple** atualiza apenas o buffer de memória. Para liberar dados, [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) ou [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (última versão) deve ser chamado.

Esse design significa que o [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) pode ter sucesso, mas os dados não são realmente gravados de forma persistente.

> [!Note]  
> Esse tamanho do fluxo do conjunto de propriedades não pode exceder 256 bytes.

 

 

 