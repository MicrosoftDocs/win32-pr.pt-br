---
title: O método IOleContainer EnumObjects
description: O método IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159399"
---
# <a name="the-iolecontainerenumobjects-method"></a><span data-ttu-id="d3e87-103">O método IOleContainer:: EnumObjects</span><span class="sxs-lookup"><span data-stu-id="d3e87-103">The IOleContainer::EnumObjects Method</span></span>

<span data-ttu-id="d3e87-104">Esse método é usado para enumerar todos os objetos OLE contidos em um documento ou formulário, retornando um ponteiro de interface para cada objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="d3e87-104">This method is used to enumerate over all the OLE objects contained in a document or form, returning an interface pointer for each OLE object.</span></span> <span data-ttu-id="d3e87-105">O contêiner deve retornar ponteiros para cada objeto OLE que compartilha o mesmo contêiner.</span><span class="sxs-lookup"><span data-stu-id="d3e87-105">The container must return pointers to each OLE object that shares the same container.</span></span> <span data-ttu-id="d3e87-106">Formulários aninhados ou controles aninhados também devem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="d3e87-106">Nested forms or nested controls must also be enumerated.</span></span>

<span data-ttu-id="d3e87-107">Alguns contêineres implementam controles de extensor, que encapsulam controles não ActiveX e, em seguida, retornam ponteiros para esses controles de extensor, pois um formulário é enumerado.</span><span class="sxs-lookup"><span data-stu-id="d3e87-107">Some containers implement extender controls, which wrap non-ActiveX controls, and then return pointers to these extender controls as a form is enumerated.</span></span> <span data-ttu-id="d3e87-108">Esse comportamento permite que controles ActiveX e contêineres de controle ActiveX se integrem bem com controles não ActiveX e, portanto, são recomendados, mas não obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d3e87-108">This behavior enables ActiveX controls and ActiveX control containers to integrate well with non-ActiveX controls, and is thus recommended, but not required.</span></span>

 

 




