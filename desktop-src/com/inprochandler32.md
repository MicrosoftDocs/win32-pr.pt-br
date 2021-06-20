---
title: InprocHandler32
description: InprocHandler32 especifica se um aplicativo usa um manipulador personalizado na chave HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID do Registro.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Chave do Registro InprocHandler32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405999"
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

Esse é um **valor \_ REG SZ** que especifica o manipulador personalizado usado pelo aplicativo. Se um manipulador personalizado não for usado, a entrada deverá ser definida como Ole32.dll.

Se um contêiner estiver pesquisando no Registro um manipulador personalizado, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 




