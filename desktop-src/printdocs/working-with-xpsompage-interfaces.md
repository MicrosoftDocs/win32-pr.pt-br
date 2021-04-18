---
description: Este tópico descreve como usar as interfaces de nível de página que fornecem acesso ao conteúdo de uma página em um OM XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Trabalhando com interfaces de página de OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764049"
---
# <a name="working-with-xps-om-page-interfaces"></a>Trabalhando com interfaces de página de OM XPS

Este tópico descreve como usar as interfaces de nível de página que fornecem acesso ao conteúdo de uma página em um OM XPS.



| Nome da interface                                                                                                                                                                              | Interfaces filho lógicas                                                                                                                                                                                            | Descrição                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | O objeto raiz do conteúdo da página.<br/> Esse objeto representa uma parte do documento.<br/>                                                |
| [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | As interfaces que derivam da interface [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) podem ser armazenadas em um dicionário de recursos e compartilhadas.<br/> |
| [**IXpsOMRemoteDictionaryResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [**IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [**IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | Contém um dicionário de recursos.<br/>                                                                                                         |
| [**IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | Nenhum<br/>                                                                                                                                                                                                     | Faz referência aos recursos que são compartilhados por outros objetos.<br/>                                                                              |
| [**IXpsOMStoryFragmentsResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | Nenhum<br/>                                                                                                                                                                                                     | Fornece acesso ao conteúdo do fluxo de recursos da parte StoryFragments do documento.<br/>                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[**Interface IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Interface IXpsOMRemoteDictionaryResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[**Interface IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[**Interface IXpsOMStoryFragmentsResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




