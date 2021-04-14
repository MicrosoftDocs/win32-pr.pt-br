---
description: Você pode adicionar suporte a parâmetros de tempo de execução a um XAPO implementando a interface IXAPOParameters. O suporte a parâmetros de tempo de execução permite que um XAPO altere seu comportamento com base nos parâmetros passados para ele em tempo de execução.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Como: Adicionar suporte de parâmetro de tempo de execução ao XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461174"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a><span data-ttu-id="d3e0d-104">Como: Adicionar suporte de parâmetro de tempo de execução ao XAPO</span><span class="sxs-lookup"><span data-stu-id="d3e0d-104">How to: Add Run-time Parameter Support to an XAPO</span></span>

<span data-ttu-id="d3e0d-105">Você pode adicionar suporte a parâmetros de tempo de execução a um XAPO implementando a interface [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) .</span><span class="sxs-lookup"><span data-stu-id="d3e0d-105">You can add run-time parameter support to an XAPO by implementing the [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interface.</span></span> <span data-ttu-id="d3e0d-106">O suporte a parâmetros de tempo de execução permite que um XAPO altere seu comportamento com base nos parâmetros passados para ele em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d3e0d-106">Run-time parameter support allows an XAPO to change its behavior based on the parameters passed to it at run time.</span></span>

1.  <span data-ttu-id="d3e0d-107">Siga as etapas em [como: criar um XAPO](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="d3e0d-107">Follow the steps in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>
2.  <span data-ttu-id="d3e0d-108">Altere o XAPO para derivar de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) e [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span><span class="sxs-lookup"><span data-stu-id="d3e0d-108">Change the XAPO to derive from [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) and [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span></span>
3.  <span data-ttu-id="d3e0d-109">Adicione chamadas para os métodos [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) e [**CXAPOParametersBase:: endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) à implementação de [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="d3e0d-109">Add calls to the methods [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) to the implementation of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

    > [!Note]  
    > <span data-ttu-id="d3e0d-110">Adicionar esses métodos a [IXAPO::P modelos](how-to--build-a-basic-audio-processing-graph.md) permite que o [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) mantenha suas cópias dos parâmetros de efeito em um estado thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d3e0d-110">Adding these methods to [IXAPO::Process](how-to--build-a-basic-audio-processing-graph.md) allows [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) to keep its copies of the effect parameters in a thread-safe state.</span></span> <span data-ttu-id="d3e0d-111">Chame [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) no início de [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process)e [**CXAPOParametersBase:: endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) no final de **IXAPO::P modelos**.</span><span class="sxs-lookup"><span data-stu-id="d3e0d-111">Call [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) at the beginning of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) at the end of **IXAPO::Process**.</span></span>

     

4.  <span data-ttu-id="d3e0d-112">Adicione mais código à implementação [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para alterar seu comportamento de acordo com os valores armazenados pelo método [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .</span><span class="sxs-lookup"><span data-stu-id="d3e0d-112">Add more code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation to change its behavior according to values stored by the [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="d3e0d-113">Adicionar código ao método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para usar os parâmetros especificados por [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) permite que o comportamento de XAPO seja alterado durante toda a vida útil.</span><span class="sxs-lookup"><span data-stu-id="d3e0d-113">Adding code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method to use the parameters specified by [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) allows the XAPO's behavior to be changed throughout its life.</span></span>

     

5.  <span data-ttu-id="d3e0d-114">Ao criar uma instância do efeito, aloque um buffer de três das estruturas que representarão os parâmetros do efeito e passe-o para o construtor [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .</span><span class="sxs-lookup"><span data-stu-id="d3e0d-114">When you create an instance of the effect, allocate a buffer of three of the structures that will represent the effect's parameters, and pass it to the [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) constructor.</span></span>

    > [!Note]  
    > <span data-ttu-id="d3e0d-115">A instância [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) usa internamente esse buffer para gerenciar os parâmetros de efeito passados a ele quando você chama [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span><span class="sxs-lookup"><span data-stu-id="d3e0d-115">The [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) instance internally uses this buffer to manage effect parameters passed to it when you call [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span></span> <span data-ttu-id="d3e0d-116">Você deve inicializar todos os blocos de parâmetro de processo em *pParameterBlocks* para o mesmo valor padrão antes de chamar qualquer um dos métodos [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters:: Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)e **IXAPOParameters:: Parameters** .</span><span class="sxs-lookup"><span data-stu-id="d3e0d-116">You must initialize all the process parameter blocks in *pParameterBlocks* to the same default value before you call any of the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters), and **IXAPOParameters::SetParameters** methods.</span></span> <span data-ttu-id="d3e0d-117">Normalmente, essa inicialização é manipulada em [**IXAPO:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) ou em [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span><span class="sxs-lookup"><span data-stu-id="d3e0d-117">Usually this initialization is handled in [**IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) or in [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="d3e0d-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3e0d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3e0d-119">Efeitos de áudio</span><span class="sxs-lookup"><span data-stu-id="d3e0d-119">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="d3e0d-120">Visão geral do XAPO</span><span class="sxs-lookup"><span data-stu-id="d3e0d-120">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
