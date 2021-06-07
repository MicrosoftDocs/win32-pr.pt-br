---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica a \_ Propriedade PKEY QuickAccessToolbarDock da interface do usuário \_ .
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e28ec2e153755fd243bf78ee389cad40485a348
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443757"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a><span data-ttu-id="35ca1-103">\_QuickAccessToolbarDock PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="35ca1-103">UI\_PKEY\_QuickAccessToolbarDock</span></span>

<span data-ttu-id="35ca1-104">Identifica a \_ Propriedade PKEY QuickAccessToolbarDock da interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="35ca1-104">Identifies the UI\_PKEY\_QuickAccessToolbarDock property.</span></span>

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a><span data-ttu-id="35ca1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="35ca1-105">Remarks</span></span>

<span data-ttu-id="35ca1-106">A interface do usuário \_ PKEY \_ QuickAccessToolbarDock é usada por um aplicativo para consultar o estado de encaixe da barra de ferramentas de acesso rápido (qat).</span><span class="sxs-lookup"><span data-stu-id="35ca1-106">UI\_PKEY\_QuickAccessToolbarDock is used by an application to query the dock-state of the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="35ca1-107">O valor da propriedade é da [**enumeração \_ CONTROLDOCK da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) .</span><span class="sxs-lookup"><span data-stu-id="35ca1-107">The property value is from the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) enumeration.</span></span>



|    <span data-ttu-id="35ca1-108">Enumeração</span><span class="sxs-lookup"><span data-stu-id="35ca1-108">Enumeration</span></span>                     |    <span data-ttu-id="35ca1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="35ca1-109">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ca1-110">\_ \_ parte superior da interface do usuário CONTROLDOCK</span><span class="sxs-lookup"><span data-stu-id="35ca1-110">UI\_CONTROLDOCK\_TOP</span></span>    | <span data-ttu-id="35ca1-111">O QAT é encaixado na área não cliente do aplicativo host da faixa de opções, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="35ca1-111">The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.</span></span>![captura de tela da barra de ferramentas de acesso rápido encaixada acima da faixa de opções na área não cliente.](images/properties/qat-docktop.png)<br/> |
| <span data-ttu-id="35ca1-113">\_CONTROLDOCK \_ inferior da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="35ca1-113">UI\_CONTROLDOCK\_BOTTOM</span></span> | <span data-ttu-id="35ca1-114">O QAT é encaixado como uma faixa visualmente integral abaixo da faixa de opções, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="35ca1-114">The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.</span></span> ![captura de tela da barra de ferramentas de acesso rápido encaixada abaixo da faixa de faixas.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="35ca1-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35ca1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35ca1-117">Propriedades da faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="35ca1-117">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

