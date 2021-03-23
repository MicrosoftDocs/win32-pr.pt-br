---
title: Diferenças no modelo de associação do Direct3D 11
description: Uma das principais decisões de design por trás da Associação DirectX12 é separá-la de outras tarefas de gerenciamento. Isso coloca alguns requisitos no aplicativo para gerenciar determinados riscos potenciais.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2785da6497fd4e775d9f88847928e7c4c08e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104526"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>Diferenças no modelo de associação do Direct3D 11

Uma das principais decisões de design por trás da Associação DirectX12 é separá-la de outras tarefas de gerenciamento. Isso coloca alguns requisitos no aplicativo para gerenciar determinados riscos potenciais.

A principal vantagem do modelo de associação D3D12 é que ele permite que os aplicativos alterem as associações de textura com frequência, sem um enorme custo de desempenho da CPU. Outros benefícios são que os sombreadores têm acesso a um número muito grande de recursos, os sombreadores não precisam saber com antecedência quantos recursos serão associados e que um modelo de associação de recursos unificados pode ser usado independentemente do fluxo de conteúdo do hardware ou dos aplicativos.

Para melhorar o desempenho, o modelo de associação não exige que o sistema acompanhe o controle de quais associações um aplicativo solicitou a GPU para usar, e há uma integração limpa entre a associação e as listas de comandos multi-threaded.

As seções a seguir listam algumas das alterações no modelo de associação de recursos desde o D3D11.

-   [Gerenciamento de residência de memória separado da Associação](#memory-residency-management-separated-from-binding)
-   [Gerenciamento de tempo de vida de objeto separado da Associação](#object-lifetime-management-separated-from-binding)
-   [Rastreamento de estado do recurso de driver separado da Associação](#driver-resource-state-tracking-separated-from-binding)
-   [Sincronização de memória mapeada da GPU de CPU separada da Associação](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [Tópicos relacionados](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>Gerenciamento de residência de memória separado da Associação

Os aplicativos têm controle explícito sobre quais superfícies precisam estar disponíveis para que a GPU seja usada diretamente (chamada de "residente"). Por outro lado, eles podem aplicar outros Estados em recursos, como torná-los explicitamente não residentes ou deixar o sistema operacional escolher para determinadas classes de aplicativos que exigem um espaço mínimo de memória. O ponto importante aqui é que o gerenciamento do aplicativo do que é residente é completamente dissociado de como ele oferece acesso aos recursos para os sombreadores.

O desacoplamento do gerenciamento de residência do mecanismo para dar acesso aos sombreadores aos recursos reduz o custo do sistema/hardware para a renderização, uma vez que o sistema operacional não precisa inspecionar constantemente o estado de associação local para saber o que tornar-se residente. Além disso, os sombreadores não precisam mais saber quais superfícies exatas talvez precisem fazer referência, desde que todo o conjunto de recursos possivelmente acessíveis tenha sido tornado residente antecipadamente.

## <a name="object-lifetime-management-separated-from-binding"></a>Gerenciamento de tempo de vida de objeto separado da Associação

Ao contrário das APIs anteriores, o sistema não rastreia mais associações de recursos para o pipeline. Isso é usado para permitir que o sistema mantenha os recursos alives que o aplicativo lançou porque eles ainda são referenciados pelo trabalho de GPU pendente.

Antes de liberar qualquer recurso, como uma textura, os aplicativos agora devem verificar se a GPU concluiu a referência a ela. Isso significa que antes de um aplicativo poder liberar com segurança um recurso, a GPU deve ter concluído a execução da lista de comandos que referencia o recurso.

## <a name="driver-resource-state-tracking-separated-from-binding"></a>Rastreamento de estado do recurso de driver separado da Associação

O sistema não inspeciona mais as associações de recursos para entender quando ocorreram transições de recursos que exigem um trabalho adicional de driver ou GPU. Um exemplo comum para muitas GPUs e drivers é ter que saber quando uma transição de superfície é usada como uma RTV (exibição de destino de renderização) para o Modo de Exibição de Recursos de sombreador (SRV). Os próprios aplicativos agora devem identificar quando as transições de recursos com as quais o sistema pode se preocupar estão acontecendo por meio de APIs dedicadas.

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>Sincronização de memória mapeada da GPU de CPU separada da Associação

O sistema não inspeciona mais as associações de recursos para entender se o processamento precisa ser atrasado porque depende de um recurso que foi mapeado para acesso à CPU, mas ainda não foi mapeado. Agora, os aplicativos têm a responsabilidade de sincronizar os acessos de memória de CPU e GPU. Para ajudar com isso, o sistema fornece mecanismos para que o aplicativo solicite o repouso de um thread de CPU até que o trabalho seja concluído. A sondagem também pode ser feita, mas pode ser menos eficiente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associação de recursos](resource-binding.md)
</dt> </dl>

 

 




