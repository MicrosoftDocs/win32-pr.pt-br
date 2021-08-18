---
description: Os SEGUINTES GUIDs de classe de manipulação direta são definidos em DirectManipulation.idl.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUIDs de Manipulação Direta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3ee67206bf9395c3a338dba27c9365578d30d7304f465d93fdc90322a77a8a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280537"
---
# <a name="direct-manipulation-guids"></a>GUIDs de Manipulação Direta

Os SEGUINTES GUIDs [de](direct-manipulation-portal.md) classe de manipulação direta são definidos em DirectManipulation.idl.

- [IDs de classe mestre](#master-class-ids)
- [IDs de classe de conteúdo secundário](#secondary-content-class-ids)
- [IDs de classe de objetos de comportamento](#behavior-objects-class-ids)
- [Tópicos relacionados](#related-topics)

## <a name="master-class-ids"></a>IDs de classe mestre

| GUID                                     | Descrição                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | Classe DirectManipulationManager. Esse objeto fornece acesso a todos os [recursos e](direct-manipulation-portal.md) APIs de Manipulação Direta disponíveis para o aplicativo.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | Classe DCompManipulationCompositor. Essa é uma implementação do [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) que envolve DirectComposition. Por meio desse objeto compositor, DirectManipulation pode aplicar a saída definindo as transformaçãos diretamente na árvore DComp. |

## <a name="secondary-content-class-ids"></a>IDs de classe de conteúdo secundário

| GUID                                  | Descrição                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ VerticalIndicatorContent**   | Indicador de panorâmico vertical. Um elemento visual que mostra sua posição atual no conteúdo que se estende para fora da tela verticalmente.     |
| **CLSID \_ HorizontalIndicatorContent** | Indicador de panorâmico horizontal. Um elemento visual que mostra sua posição atual no conteúdo que se estende horizontalmente para fora da tela. |
| **CLSID \_ VirtualViewportContent**     | Virtual Viewport. Um viewport virtual pode ser usado para respeitar elementos de posição fixa para viewports com zoom configurado.          |

## <a name="behavior-objects-class-ids"></a>IDs de classe de objetos de comportamento

| GUID                                     | Descrição                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ DragDropConfigurationBehavior** | Arraste & comportamento de soltar. Permite que os itens sejam selecionados e arrastados.                                                                                       |
| **CLSID \_ AutoScrollBehavior**            | Comportamento de autoscroll. Permite que o conteúdo role automaticamente conforme ele se aproxima do limite de um determinado eixo.                                           |
| **CLSID \_ DeferContactService**           | Contate o comportamento de adiamento. A quantidade de tempo (em milissegundos) a aguardar antes de chamar [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). |

## <a name="related-topics"></a>Tópicos relacionados

[Manipulação direta,](direct-manipulation-portal.md) [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**AddConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration) [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
