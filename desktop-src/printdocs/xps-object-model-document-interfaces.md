---
description: As interfaces de documento fornecem acesso aos componentes do pacote XPS que determinam a estrutura de um documento em um OM XPS.
ms.assetid: 3302d164-81ad-4198-a116-f967e7a14147
title: Interfaces de documento do XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc191c4c0b8ec5571331022321a8ae829587022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749165"
---
# <a name="xps-om-document-interfaces"></a>Interfaces de documento do XPS OM

As interfaces de documento fornecem acesso aos componentes do pacote XPS que determinam a estrutura de um documento em um OM XPS. A tabela a seguir lista as interfaces de documento do.



| Nome da interface                                                      | Interfaces filho lógicas                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>           | Representa um conjunto de documentos vinculados em uma lista ordenada.<br/> As interfaces filhas são coletadas em uma interface [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection) .<br/>                                                                                                                                                                                                  |
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Representa uma única parte de FixedDocument e associa a coleção de referências de página das páginas de um documento.<br/> As interfaces filhas são coletadas em uma interface [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) .<br/> A estrutura do documento é exposta em uma interface [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource) .<br/> |
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                   | Uma versão virtualizada leve de uma página no documento. Uma referência de página descreve as principais características da página (como suas dimensões), mas não inclui nenhum conteúdo da página.<br/>                                                                                                                                                                                             |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/>     | Nenhum<br/>                                               | Uma coleção de objetos da página que são destinos de hiperlink.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>       | Nenhum<br/>                                               | Uma coleção dos recursos da parte que estão associados a uma página.<br/>                                                                                                                                                                                                                                                                                                                                |



 

## <a name="contents"></a>Sumário

-   [Trabalhar com interfaces IXpsOMDocumentSequence](working-with-xpsomdocumentsequence-interfaces.md) contém informações sobre como usar as seguintes interfaces:
    -   [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
    -   [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
-   [Trabalhar com interfaces IXpsOMDocument](working-with-xpsomdocument-interfaces.md) contém informações sobre como usar as seguintes interfaces:
    -   [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
    -   [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
    -   [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
-   [Trabalhar com interfaces IXpsOMPageReference](working-with-xpsompagereference-interfaces.md) contém informações sobre como usar as seguintes interfaces:
    -   [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
    -   [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
    -   [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
    -   [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)

 

 




