---
title: InprocHandler32
description: Especifica se um aplicativo usa um manipulador personalizado.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- InprocHandler32 de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363774"
---
# <a name="inprochandler32"></a>InprocHandler32

Especifica se um aplicativo usa um manipulador personalizado.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz de reg** que especifica o manipulador personalizado usado pelo aplicativo. Se um manipulador personalizado não for usado, a entrada deverá ser definida como Ole32.dll.

Se um contêiner estiver pesquisando o registro em busca de um manipulador personalizado, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 




