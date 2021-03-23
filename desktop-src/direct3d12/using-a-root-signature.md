---
title: Usando uma assinatura de raiz
description: A assinatura raiz é a definição de uma coleção organizada arbitrariamente de tabelas de descritores (incluindo seu layout), constantes raiz e descritores raiz.
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3babe26dc06d4f85ce3d6fb771e18c78b54a3701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104778"
---
# <a name="using-a-root-signature"></a>Usando uma assinatura de raiz

A assinatura raiz é a definição de uma coleção organizada arbitrariamente de tabelas de descritores (incluindo seu layout), constantes raiz e descritores raiz. Cada entrada tem um custo em direção a um limite máximo, portanto, o aplicativo pode compensar o equilíbrio entre o número de cada tipo de entrada que a assinatura raiz conterá.

-   [Semântica de lista de comandos](#command-list-semantic)
-   [Semântica do pacote](#bundle-semantics)
-   [Tópicos relacionados](#related-topics)

A assinatura raiz é um objeto que pode ser criado pela especificação manual na API. Todos os sombreadores em um PSO devem ser compatíveis com o layout raiz especificado com o PSO ou os sombreadores individuais devem incluir layouts de raiz incorporados que correspondam uns aos outros; caso contrário, haverá falha na criação do PSO. Uma propriedade da assinatura raiz é que os sombreadores não precisam saber sobre ele quando criados, embora as assinaturas raiz também possam ser criadas diretamente em sombreadores, se desejado. Os ativos de sombreador existentes não exigem nenhuma alteração para serem compatíveis com as assinaturas raiz. O Shader Model 5,1 é introduzido para fornecer uma flexibilidade extra (indexação dinâmica de descritores de dentro de sombreadores) e pode ser adotado incrementalmente a partir de ativos de sombreador existentes, conforme desejado.

## <a name="command-list-semantic"></a>Semântica de lista de comandos

No início de uma lista de comandos, a assinatura raiz é indefinida. Os sombreadores de gráficos têm uma assinatura de raiz separada do sombreador de computação, cada um atribuído de forma independente em uma lista de comandos. A assinatura raiz definida em uma lista de comandos ou um pacote também deve corresponder ao PSO definido no momento em empate/Dispatch; caso contrário, o comportamento será indefinido. Incompatibilidades de assinatura de raiz transitória antes de desenhar/distribuir são boas, como definir um PSO incompatível antes de alternar para uma assinatura raiz compatível (desde que eles sejam compatíveis com o tempo que o empate/expedição seja chamado). A definição de um PSO não altera a assinatura raiz. O aplicativo deve chamar uma API dedicada para definir a assinatura raiz.

Depois que uma assinatura de raiz tiver sido definida em uma lista de comandos, o layout definirá o conjunto de associações que o aplicativo deve fornecer e qual PSOs poderá ser usado (aqueles compilados com o mesmo layout) para as próximas chamadas de emissão/expedição. Por exemplo, uma assinatura raiz pode ser definida pelo aplicativo para ter as seguintes entradas. Cada entrada é chamada de "slot".

-   \[0 \] um descritor cbv embutido (inscriprs raiz)
-   \[1 \] uma tabela de descritores contendo 2 SRVs, 1 CBVs e 1 UAV
-   \[2 \] uma tabela de descritores contendo 1 amostra
-   \[3 \] uma coleção 4x32 de constantes de raiz
-   \[4 \] uma tabela de descritores contendo um número não especificado de SRVs

Nesse caso, antes de poder emitir um empate/expedição, espera-se que o aplicativo defina a ligação apropriada para cada um dos slots \[ 0.. 4 \] que o aplicativo definiu com sua assinatura raiz atual. Por exemplo, no slot \[ 1 \] , uma tabela de descritores deve ser associada, que é uma região contígua em um heap de descritor que contém (ou conterá na execução) 2 SRVs, 1 CBVs e 1 UAV. Da mesma forma, as tabelas de descritores devem ser definidas nos slots \[ 2 \] e \[ 4 \] .

O aplicativo pode alterar parte das associações de assinatura raiz de cada vez (o restante permanece inalterado). Por exemplo, se a única coisa que precisa ser alterada entre o desenho for uma das constantes no slot \[ 2 \] , isso é tudo o que o aplicativo precisa para reassociar. Conforme discutido anteriormente, as versões de driver/hardware de todos os Estados de ligação de assinatura de raiz, conforme são modificadas automaticamente. Se uma assinatura de raiz for alterada em uma lista de comandos, todas as associações de assinatura de raiz anteriores se tornarão obsoletas e todas as associações esperadas deverão ser definidas antes de desenhar/distribuir; caso contrário, o comportamento será indefinido. Se a assinatura raiz estiver definida com redundância para a mesma definida atualmente, as associações de assinatura raiz existentes não se tornarão obsoletas.

## <a name="bundle-semantics"></a>Semântica do pacote

Os grupos herdam as associações de assinatura raiz da lista de comandos (as associações para os vários slots no exemplo de lista de comandos acima). Se um pacote precisar alterar algumas das associações de assinatura raiz herdadas, primeiro será necessário definir a assinatura raiz como a mesma que a lista de comandos de chamada (as associações herdadas não se tornarão obsoletas). Se o pacote definir a assinatura raiz para ser diferente da lista de comandos de chamada, que tem o mesmo efeito que alterar a assinatura raiz na lista de comandos descrita acima: todas as associações de assinatura raiz anteriores são obsoletas e as associações esperadas recentemente devem ser definidas antes de desenhar/distribuir; caso contrário, o comportamento será indefinido. Se um pacote não precisar alterar nenhuma associação de assinatura raiz, ele não precisará definir a assinatura raiz.

O código a seguir mostra um fluxo de chamada de exemplo em um pacote.

``` syntax
// Command List
...
pCmdList->SetGraphicsRootSignature(pRootSig); // new parameter space
MyEngine_SetTextures(); // bundle inherits descriptor table setting
MyEngine_SetAnimationFactor(fTime); // bundle inherits root constant
pCmdList->ExecuteBundle(...);
...
// Bundle
pBundle->SetGraphicsRootSignature(pRootSig); // same as caller, in order to inherits bindings
pBundle->SetPipelineState(pPS); 
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,0,drawIDOffset);
pBundle->Draw(...); // using inherited textures / animation factor
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,1,drawIDOffset);
pBundle->Draw(...);
...
```

Saindo de um pacote, todas as alterações de layout raiz e/ou alterações de associação de um pacote são herdadas de volta para a lista de comandos de chamada quando um pacote termina de ser executado.

Para obter mais informações sobre herança, consulte a seção **herança de estado de pipeline de gráficos** de [Gerenciando o estado do pipeline de gráficos no Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> </dl>

 

 




