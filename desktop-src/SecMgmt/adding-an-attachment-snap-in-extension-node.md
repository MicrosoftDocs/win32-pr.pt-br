---
description: Uma extensão de snap-in de anexo deve ser adicionada no nó serviços quando esse nó é expandido por um usuário.
ms.assetid: af853c29-11c2-4fd0-ad81-80aebeb74cc3
title: Adicionando um nó de extensão de snap-in de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2604a58284af7bc55ff57ae114bc77d8f0cd42ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662667"
---
# <a name="adding-an-attachment-snap-in-extension-node"></a><span data-ttu-id="c7aaf-103">Adicionando um nó de extensão de snap-in de anexo</span><span class="sxs-lookup"><span data-stu-id="c7aaf-103">Adding an Attachment Snap-in Extension Node</span></span>

<span data-ttu-id="c7aaf-104">Uma extensão de snap-in de anexo deve ser adicionada no nó serviços quando esse nó é expandido por um usuário.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-104">An attachment snap-in extension must add itself under the Services node when that node is expanded by a user.</span></span>

<span data-ttu-id="c7aaf-105">Quando um usuário expande o nó serviços em um dos snap-ins de configuração de segurança, o MMC usa [**IComponentData:: Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) e a mensagem de notificação de expansão do MMCN \_ para notificar o snap-in de configuração de segurança, além de todas as suas extensões.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-105">When a user expands the Services node under one of the Security Configuration snap-ins, MMC uses [**IComponentData::Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) and the MMCN\_EXPAND notification message to notify the Security Configuration snap-in, plus all its extensions.</span></span>

<span data-ttu-id="c7aaf-106">Em seguida, o snap-in de configuração de segurança extrai seu formato interno do *lpDataObject*, que é passado da estrutura principal do MMC como o tipo **lpDataObject**.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-106">The Security Configuration snap-in then extracts its internal format from the *lpDataObject*, which is passed in from the MMC main framework as type **LPDATAOBJECT**.</span></span> <span data-ttu-id="c7aaf-107">Ele para de processar quando vê o tipo de nó serviços.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-107">It stops processing when it sees the Services node type.</span></span> <span data-ttu-id="c7aaf-108">Em seguida, a extensão do snap-in de anexos extrai o tipo de nó do *lpDataObject*.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-108">The attachment snap-in extension then extracts the node type from the *lpDataObject*.</span></span> <span data-ttu-id="c7aaf-109">Se o tipo de nó for um dos tipos de nó definidos pelo serviço, a extensão de snap-in de anexos inserirá seus nós raiz no nó pai especificado.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-109">If the node type is one of the service's defined node types, the attachment snap-in extension inserts its root nodes under the specified parent node.</span></span>

<span data-ttu-id="c7aaf-110">Observe que, neste exemplo, ExtractNodeType é uma função particular que a extensão implementa.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-110">Note that in this example, ExtractNodeType, is a private function that the extension implements.</span></span> <span data-ttu-id="c7aaf-111">A extensão examina o objeto de dados para obter o tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-111">The extension examines the data object to get the node type.</span></span> <span data-ttu-id="c7aaf-112">A implementação de ExtractNodeType não é mostrada.</span><span class="sxs-lookup"><span data-stu-id="c7aaf-112">The implementation of ExtractNodeType is not shown.</span></span>


```C++
//  Detect which extension node to expand.
GUID* nodeType = ExtractNodeType(lpdataObject);

if (NULL == nodeType)
{
  return S_OK;
}

if (TRUE == ::IsEqualGUID(*nodeType, cNodetypeSceTemplateServices))
{
  folderType = ATTACHMENT_STATIC;  // defined by attachment writer
}

else if (TRUE == ::IsEqualGUID
    (*nodeType, cNodetypeSceAnalysisServices))
{
  folderType = ATTACHMENT_STATIC_ANALYSIS;
               // defined by attachment writer
}

//  Free resources.
::GlobalFree(reinterpret_cast<HANDLE>(nodeType));

//  Add service attachment root node and remember it as the
//  root of the SMB extension namespace.
//  ...
```



 

 
