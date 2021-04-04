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
# <a name="adding-an-attachment-snap-in-extension-node"></a>Adicionando um nó de extensão de snap-in de anexo

Uma extensão de snap-in de anexo deve ser adicionada no nó serviços quando esse nó é expandido por um usuário.

Quando um usuário expande o nó serviços em um dos snap-ins de configuração de segurança, o MMC usa [**IComponentData:: Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) e a mensagem de notificação de expansão do MMCN \_ para notificar o snap-in de configuração de segurança, além de todas as suas extensões.

Em seguida, o snap-in de configuração de segurança extrai seu formato interno do *lpDataObject*, que é passado da estrutura principal do MMC como o tipo **lpDataObject**. Ele para de processar quando vê o tipo de nó serviços. Em seguida, a extensão do snap-in de anexos extrai o tipo de nó do *lpDataObject*. Se o tipo de nó for um dos tipos de nó definidos pelo serviço, a extensão de snap-in de anexos inserirá seus nós raiz no nó pai especificado.

Observe que, neste exemplo, ExtractNodeType é uma função particular que a extensão implementa. A extensão examina o objeto de dados para obter o tipo de nó. A implementação de ExtractNodeType não é mostrada.


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



 

 
