---
description: Para impulsionar atualizações visuais, o aplicativo deve usar IDirectManipulationCompositor.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Mecanismo de composição
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 14bc2ad60405dba7874493096e022b553a8b276cd6f0bb21ea9ae3cf191f5d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117896"
---
# <a name="composition-engine"></a>Mecanismo de composição

Para impulsionar atualizações visuais, o aplicativo deve usar [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor). Esse objeto é responsável por atualizar [](direct-manipulation-portal.md) visuais com base em atualizações de Manipulação Direta, impulsionar atualizações de inércia e fornecer informações de tempo de composição para Manipulação Direta Além disso, um aplicativo deve usar o [DCompManipulationCompositor](direct-manipulation-guids.md) fornecido pela Manipulação [Direta,](direct-manipulation-portal.md)que manipulará todas as atualizações visuais em nome do aplicativo e direcionará as atualizações de inércia.

O [DCompManipulationCompositor](direct-manipulation-guids.md) é uma implementação da interface [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) que envolve [DirectComposition.](../directcomp/directcomposition-portal.md) Em vez de fazer com que o [](direct-manipulation-portal.md) aplicativo aplique a saída, por meio desse objeto compositor, a Manipulação Direta pode aplicar a saída definindo as transformação diretamente na árvore DirectComposition. Usando essa configuração, a entrada pode ser processada e as transformação de saída podem ser aplicadas, independentemente da atividade no thread da interface do usuário.

Para dar [informações de](direct-manipulation-portal.md) Manipulação Direta sobre o tempo do mecanismo de composição, a classe [DCompManipulationCompositor](direct-manipulation-guids.md) implementa a interface [**IDirectManipulationFrameInfoProvider.**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) Ao criar um viewport, [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) o ponteiro [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) obtido de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para uma instância **de IDirectManipulationFrameInfoProvider**. O **ponteiro IDirectManipulationFrameInfoProvider** é passado para a [**função IDirectManipulationManager::CreateViewport().**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport)
