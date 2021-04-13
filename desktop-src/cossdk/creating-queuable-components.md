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
# <a name="creating-queuable-components"></a><span data-ttu-id="ddfbe-103">Criando componentes do Queuable</span><span class="sxs-lookup"><span data-stu-id="ddfbe-103">Creating Queuable Components</span></span>

<span data-ttu-id="ddfbe-104">Um componente com pelo menos uma interface queuable é um *componente queuable*.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-104">A component with at least one queuable interface is a *queuable component*.</span></span> <span data-ttu-id="ddfbe-105">Para que um componente seja invocado por uma fila, as interfaces devem ser marcadas como queuable e o componente deve ser instalado em um aplicativo enfileirado.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-105">For a component to be invoked by a queue, the interfaces must be marked as queuable and the component must be installed in a queued application.</span></span> <span data-ttu-id="ddfbe-106">No entanto, um componente queuable pode ser um componente de um aplicativo não enfileirado.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-106">However, a queuable component can be a component of a non-queued application.</span></span>

<span data-ttu-id="ddfbe-107">Uma interface queuable deve conter apenas em parâmetros, sem parâmetros de saída e nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-107">A queuable interface must contain only in parameters—no out parameters and no return values.</span></span> <span data-ttu-id="ddfbe-108">Essas características são verificadas analisando as informações de tipo durante a instalação do componente.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-108">These characteristics are verified by analyzing the type information during component installation.</span></span> <span data-ttu-id="ddfbe-109">Se a interface não for queuable, a fila do aplicativo que contém o componente não poderá ser ativada.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-109">If the interface is not queuable, the queue of the application containing the component cannot be activated.</span></span>

<span data-ttu-id="ddfbe-110">Para especificar uma interface COM+ como queuable, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ddfbe-110">To specify a COM+ interface as queuable, use the following steps:</span></span>

1.  <span data-ttu-id="ddfbe-111">Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="ddfbe-112">Abra a pasta **interfaces** do componente do aplicativo com+ que você deseja tornar queuable.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-112">Open the **Interfaces** folder of the component of the COM+ application that you want to make queuable.</span></span>

3.  <span data-ttu-id="ddfbe-113">Clique com o botão direito do mouse na interface que você deseja marcar como queuable e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-113">Right-click the interface that you want to mark as queuable, and then click **Properties**.</span></span>

4.  <span data-ttu-id="ddfbe-114">Selecione a guia **enfileiramento** na caixa de diálogo Propriedades.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-114">Select the **Queuing** tab in the properties dialog.</span></span>

5.  <span data-ttu-id="ddfbe-115">Ative a caixa de seleção rotulada **na fila**.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-115">Activate the check box labeled **Queued**.</span></span>

    > [!Note]  
    > <span data-ttu-id="ddfbe-116">Se a caixa de seleção **na fila** estiver esmaecida, a interface não atenderá às restrições de queuable descritas acima.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-116">If the **Queued** check box is grayed out, the interface does not satisfy the queuable constraints described above.</span></span>

     

6.  <span data-ttu-id="ddfbe-117">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-117">Click **OK**.</span></span>

    <span data-ttu-id="ddfbe-118">Um componente queuable pode ser identificado como tal adicionando a macro de atributo de fila à seção de interface do arquivo de origem IDL (Interface Definition Language) para todas as interfaces que são queuable.</span><span class="sxs-lookup"><span data-stu-id="ddfbe-118">A queuable component can be identified as such by adding the QUEUEABLE attribute macro to the Interface section of the Interface Definition Language (IDL) source file for all interfaces that are queuable.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ddfbe-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddfbe-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddfbe-120">Criando filas de componentes</span><span class="sxs-lookup"><span data-stu-id="ddfbe-120">Creating Component Queues</span></span>](creating-component-queues.md)
</dt> <dt>

[<span data-ttu-id="ddfbe-121">Desenvolvendo componentes em fila</span><span class="sxs-lookup"><span data-stu-id="ddfbe-121">Developing Queued Components</span></span>](developing-queued-components.md)
</dt> </dl>

 

 



