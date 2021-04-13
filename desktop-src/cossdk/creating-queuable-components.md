---
description: Um componente com pelo menos uma interface queuable é um componente queuable.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Criando componentes do Queuable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370427"
---
# <a name="creating-queuable-components"></a>Criando componentes do Queuable

Um componente com pelo menos uma interface queuable é um *componente queuable*. Para que um componente seja invocado por uma fila, as interfaces devem ser marcadas como queuable e o componente deve ser instalado em um aplicativo enfileirado. No entanto, um componente queuable pode ser um componente de um aplicativo não enfileirado.

Uma interface queuable deve conter apenas em parâmetros, sem parâmetros de saída e nenhum valor de retorno. Essas características são verificadas analisando as informações de tipo durante a instalação do componente. Se a interface não for queuable, a fila do aplicativo que contém o componente não poderá ser ativada.

Para especificar uma interface COM+ como queuable, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.

2.  Abra a pasta **interfaces** do componente do aplicativo com+ que você deseja tornar queuable.

3.  Clique com o botão direito do mouse na interface que você deseja marcar como queuable e clique em **Propriedades**.

4.  Selecione a guia **enfileiramento** na caixa de diálogo Propriedades.

5.  Ative a caixa de seleção rotulada **na fila**.

    > [!Note]  
    > Se a caixa de seleção **na fila** estiver esmaecida, a interface não atenderá às restrições de queuable descritas acima.

     

6.  Clique em **OK**.

    Um componente queuable pode ser identificado como tal adicionando a macro de atributo de fila à seção de interface do arquivo de origem IDL (Interface Definition Language) para todas as interfaces que são queuable.

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando filas de componentes](creating-component-queues.md)
</dt> <dt>

[Desenvolvendo componentes em fila](developing-queued-components.md)
</dt> </dl>

 

 



