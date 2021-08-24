---
description: Um componente com pelo menos uma interface envelhável é um componente que pode ser envelhável.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Criando componentes envelháveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ca7b4717da44145121508ed3e8b208e8401a240f1a2ceb858be299bf2b32f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637836"
---
# <a name="creating-queuable-components"></a>Criando componentes envelháveis

Um componente com pelo menos uma interface envelhável é *um componente que pode ser envelhável.* Para que um componente seja invocado por uma fila, as interfaces devem ser marcadas como na fila e o componente deve ser instalado em um aplicativo na fila. No entanto, um componente que pode ser envelhável pode ser um componente de um aplicativo que não está na fila.

Uma interface que pode ser envelhável deve conter somente em parâmetros – sem parâmetros de saída e sem valores de retorno. Essas características são verificadas analisando as informações de tipo durante a instalação do componente. Se a interface não for enfilável, a fila do aplicativo que contém o componente não poderá ser ativada.

Para especificar uma interface COM+ como envelhável, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em Serviços de Componentes, abra a pasta Aplicativos **COM+** associada ao computador que você deseja gerenciar.

2.  Abra a **pasta Interfaces** do componente do aplicativo COM+ que você deseja tornar na fila.

3.  Clique com o botão direito do mouse na interface que você deseja marcar como envelhável e clique em **Propriedades**.

4.  Selecione a **guia Ensuamento** na caixa de diálogo propriedades.

5.  Ative a caixa de seleção rotulada **Como en fila.**

    > [!Note]  
    > Se a **caixa de seleção Ensuada** estiver es cinza, a interface não atenderá às restrições que podem ser envelháveis descritas acima.

     

6.  Clique em **OK**.

    Um componente que pode ser enfilhável pode ser identificado como tal adicionando a macro de atributo QUEUEABLE à seção Interface do arquivo de origem IDL (Linguagem de Definição de Interface) para todas as interfaces que podem ser enfiloadas.

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

[Desenvolvendo componentes na fila](developing-queued-components.md)
</dt> </dl>

 

 



