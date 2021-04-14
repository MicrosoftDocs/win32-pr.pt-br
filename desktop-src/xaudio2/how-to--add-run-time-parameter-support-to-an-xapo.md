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
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>Como: Adicionar suporte de parâmetro de tempo de execução ao XAPO

Você pode adicionar suporte a parâmetros de tempo de execução a um XAPO implementando a interface [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . O suporte a parâmetros de tempo de execução permite que um XAPO altere seu comportamento com base nos parâmetros passados para ele em tempo de execução.

1.  Siga as etapas em [como: criar um XAPO](how-to--create-an-xapo.md).
2.  Altere o XAPO para derivar de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) e [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).
3.  Adicione chamadas para os métodos [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) e [**CXAPOParametersBase:: endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) à implementação de [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

    > [!Note]  
    > Adicionar esses métodos a [IXAPO::P modelos](how-to--build-a-basic-audio-processing-graph.md) permite que o [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) mantenha suas cópias dos parâmetros de efeito em um estado thread-safe. Chame [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) no início de [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process)e [**CXAPOParametersBase:: endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) no final de **IXAPO::P modelos**.

     

4.  Adicione mais código à implementação [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para alterar seu comportamento de acordo com os valores armazenados pelo método [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .

    > [!Note]  
    > Adicionar código ao método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para usar os parâmetros especificados por [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) permite que o comportamento de XAPO seja alterado durante toda a vida útil.

     

5.  Ao criar uma instância do efeito, aloque um buffer de três das estruturas que representarão os parâmetros do efeito e passe-o para o construtor [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

    > [!Note]  
    > A instância [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) usa internamente esse buffer para gerenciar os parâmetros de efeito passados a ele quando você chama [**Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters). Você deve inicializar todos os blocos de parâmetro de processo em *pParameterBlocks* para o mesmo valor padrão antes de chamar qualquer um dos métodos [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters:: Parameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)e **IXAPOParameters:: Parameters** . Normalmente, essa inicialização é manipulada em [**IXAPO:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) ou em [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Visão geral do XAPO](xapo-overview.md)
</dt> </dl>

 

 
