---
description: Para orientar as atualizações visuais, o aplicativo deve usar IDirectManipulationCompositor.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Mecanismo de composição
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: aa4d922893472c1fe235bae60e41a00924d13bba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456594"
---
# <a name="composition-engine"></a>Mecanismo de composição

Para orientar as atualizações visuais, o aplicativo deve usar [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor). Esse objeto é responsável pela atualização de visuais com base em atualizações de [manipulação direta](direct-manipulation-portal.md) , orientando as atualizações de inércia e fornecendo informações de tempo de composição para manipulação direta, além disso, um aplicativo deve usar o [DCompManipulationCompositor](direct-manipulation-guids.md) fornecido pela [manipulação direta](direct-manipulation-portal.md), que manipulará todas as atualizações visuais em nome do aplicativo e orientará as atualizações de inércia.

O [DCompManipulationCompositor](direct-manipulation-guids.md) é uma implementação da interface [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) que encapsula [DirectComposition](../directcomp/directcomposition-portal.md). Em vez de fazer com que o aplicativo aplique a saída, por meio dessa [manipulação direta](direct-manipulation-portal.md) de objeto compositor pode aplicar a saída definindo as transformações diretamente na árvore DirectComposition. Usando essa configuração, a entrada pode ser processada e as transformações de saída podem ser aplicadas, independentemente da atividade no thread da interface do usuário.

Para fornecer informações de [manipulação direta](direct-manipulation-portal.md) no momento do mecanismo de composição, a classe [DCompManipulationCompositor](direct-manipulation-guids.md) implementa a interface [**IDirectManipulationFrameInfoProvider**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) . Ao criar um visor, [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) o ponteiro [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) obtido de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para uma instância de **IDirectManipulationFrameInfoProvider**. O ponteiro **IDirectManipulationFrameInfoProvider** é passado para a função [**IDirectManipulationManager:: createviewport ()**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) .
