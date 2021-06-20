---
title: InprocHandler
description: InprocHandler especifica se um aplicativo usa um manipulador personalizado na HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID do Registro.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Chave do Registro InprocHandler COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404729"
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

Esse é um **valor \_ REG SZ** que especifica o manipulador personalizado usado pelo aplicativo. Se um manipulador personalizado não for usado, a entrada deverá ser definida como Ole32.dll.

Se um contêiner estiver pesquisando no Registro um manipulador personalizado, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




