---
title: Protocolo
description: Indica que esta classe OLE 2 é insertável em contêineres de OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Chave do registro de protocolo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793706"
---
# <a name="protocol"></a>Protocolo

Indica que esta classe OLE 2 é insertável em contêineres de OLE 1.

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

A entrada **StdFileEditing** especifica informações de compatibilidade de OLE 1. Ele deve estar presente somente se os objetos dessa classe forem insertáveis em contêineres de OLE 1.

**Servidor** especifica o caminho completo para o aplicativo de servidor OLE 2 e o **verbo** especifica os verbos. O verbo 0 é o verbo primário e os verbos adicionais devem ser numerados consecutivamente.

 

 




