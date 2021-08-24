---
title: Protocolo
description: Indica que essa classe OLE 2 pode ser inserida em contêineres OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Chave do Registro de Protocolo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7721e4f90a122fcbc519163d80c1e8e549f2b6aa05526d33d9693783abd1276a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130018"
---
# <a name="protocol"></a>Protocolo

Indica que essa classe OLE 2 pode ser inserida em contêineres OLE 1.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a>Comentários

A **entrada StdFileEditing** especifica informações de compatibilidade do OLE 1. Ele deverá estar presente somente se os objetos dessa classe podem ser inseridos em contêineres OLE 1.

**O** servidor especifica o caminho completo para o aplicativo de servidor OLE 2 e **Verb** especifica os verbos. O verbo 0 é o verbo primário e verbos adicionais devem ser numerados consecutivamente.

 

 




