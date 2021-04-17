---
description: Os GUIDs de classe de manipulação direta a seguir são definidos em DirectManipulation. idl.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUIDs de manipulação direta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 57dfa5701d7f01a9738206e7a2e3d669f6cf6a4a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105790438"
---
# <a name="direct-manipulation-guids"></a>GUIDs de manipulação direta

Os GUIDs de classe de [manipulação direta](direct-manipulation-portal.md) a seguir são definidos em DirectManipulation. idl.

- [Classe mestra-IDs](#master-class-ids)
- [Classe de conteúdo secundária-IDs](#secondary-content-class-ids)
- [Classes de objetos de comportamento-IDs](#behavior-objects-class-ids)
- [Tópicos relacionados](#related-topics)

## <a name="master-class-ids"></a>Classe mestra-IDs

| GUID                                     | Descrição                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | Classe DirectManipulationManager. Este objeto fornece acesso a todos os recursos de [manipulação direta](direct-manipulation-portal.md) e APIs disponíveis para o aplicativo.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | Classe DCompManipulationCompositor. Esta é uma implementação do [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) que encapsula DirectComposition. Por meio desse objeto compositor, DirectManipulation pode aplicar a saída definindo transformações diretamente na árvore DComp. |

## <a name="secondary-content-class-ids"></a>Classe de conteúdo secundária-IDs

| GUID                                  | Descrição                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **\_VERTICALINDICATORCONTENT CLSID**   | Indicador de panorâmica vertical. Um elemento visual que mostra sua posição atual no conteúdo que se estende verticalmente fora da tela.     |
| **\_HORIZONTALINDICATORCONTENT CLSID** | Indicador de panorâmica horizontal. Um elemento visual que mostra sua posição atual no conteúdo que se estende horizontalmente fora da tela. |
| **\_VIRTUALVIEWPORTCONTENT CLSID**     | Visor virtual. Um visor virtual pode ser usado para respeitar elementos de posição fixa para visores com zoom configurado.          |

## <a name="behavior-objects-class-ids"></a>Classes de objetos de comportamento-IDs

| GUID                                     | Descrição                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DRAGDROPCONFIGURATIONBEHAVIOR CLSID** | Arraste & o comportamento de soltar. Permite que os itens sejam selecionados e arrastados.                                                                                       |
| **\_AUTOSCROLLBEHAVIOR CLSID**            | Comportamento de AutoScroll. Permite que o conteúdo role automaticamente à medida que ele se aproxima do limite de um determinado eixo.                                           |
| **\_DEFERCONTACTSERVICE CLSID**           | Contate o comportamento de adiamento. A quantidade de tempo (em millliseconds) a aguardar antes de chamar [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). |

## <a name="related-topics"></a>Tópicos relacionados

[Manipulação direta](direct-manipulation-portal.md), [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**AddConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration), [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
