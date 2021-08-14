---
description: Você pode adicionar suporte a parâmetros de tempo de execução a um XAPO implementando a interface IXAPOParameters. O suporte a parâmetros em tempo de executar permite que um XAPO altere seu comportamento com base nos parâmetros passados para ele em tempo de operação.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Como: Adicionar suporte de parâmetro de tempo de execução ao XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf69fcc2570e26f188766a7f908a76d0dfcf3ec190d9fd0d7a1c434b242fdf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805536"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>Como: Adicionar suporte de parâmetro de tempo de execução ao XAPO

Você pode adicionar suporte a parâmetros de tempo de execução a um XAPO implementando a interface [**IXAPOParameters.**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) O suporte a parâmetros em tempo de executar permite que um XAPO altere seu comportamento com base nos parâmetros passados para ele em tempo de operação.

1.  Siga as etapas em [Como criar um XAPO.](how-to--create-an-xapo.md)
2.  Altere o XAPO para derivar [**de CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) e [**CXAPOBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
3.  Adicione chamadas aos métodos [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) e [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) à implementação de [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

    > [!Note]  
    > Adicionar esses métodos a [IXAPO::P rocess](how-to--build-a-basic-audio-processing-graph.md) permite que [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) mantenha suas cópias dos parâmetros de efeito em um estado thread-safe. Chame [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) no início de [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)e [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) no final de **IXAPO::P rocess**.

     

4.  Adicione mais código à implementação [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para alterar seu comportamento de acordo com os valores armazenados pelo [**método SetParameters.**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters)

    > [!Note]  
    > Adicionar código ao método [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para usar os parâmetros especificados por [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) permite que o comportamento do XAPO seja alterado ao longo de sua vida.

     

5.  Ao criar uma instância do efeito, aloce um buffer de três das estruturas que representarão os parâmetros do efeito e passe-o para o construtor [**CXAPOParametersBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)

    > [!Note]  
    > A [**instância CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) usa internamente esse buffer para gerenciar parâmetros de efeito passados para ela quando você chama [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters). Você deve inicializar todos os blocos de parâmetro de processo em *pParameterBlocks* para o mesmo valor padrão antes de chamar qualquer um dos métodos [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)e **IXAPOParameters::SetParameters.** Normalmente, essa inicialização é tratada [**em IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) ou em [**IXAPO::LockForProcess.**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Visão geral do XAPO](xapo-overview.md)
</dt> </dl>

 

 
