---
title: Conversão
description: Usado pela caixa de diálogo Converter para determinar os formatos que um aplicativo pode ler e gravar.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Conversão da chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498805"
---
# <a name="conversion"></a>Conversão

Usado pela caixa de diálogo **converter** para determinar os formatos que um aplicativo pode ler e gravar.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a>Comentários

As informações de conversão são usadas pela caixa de diálogo **converter** para determinar quais formatos um aplicativo pode ler e gravar. Um formato de arquivo delimitado por vírgula é indicado por um número, se for um dos formatos de área de transferência definidos em Windows. h. Uma cadeia de caracteres indica que o formato não é um definido no Windows. h (privado). Nesse caso, o formato legível e gravável é a \_ estrutura de tópicos do CF (privado).

O valor *rformat* especifica o formato de arquivo que um aplicativo pode ler (converter de).

O valor *rwformat* especifica o formato de arquivo que um aplicativo pode ler e gravar (ativar como).

 

 




