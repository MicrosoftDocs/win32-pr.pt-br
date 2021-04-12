---
title: InprocHandler
description: Especifica se um aplicativo usa um manipulador personalizado.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364256"
---
# <a name="inprochandler"></a>InprocHandler

Especifica se um aplicativo usa um manipulador personalizado.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz de reg** que especifica o manipulador personalizado usado pelo aplicativo. Se um manipulador personalizado não for usado, a entrada deverá ser definida como Ole32.dll.

Se um contêiner estiver pesquisando o registro em busca de um manipulador personalizado, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




