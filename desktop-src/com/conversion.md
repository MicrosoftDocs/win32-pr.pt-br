---
title: Conversão
description: Usado pela caixa de diálogo Converter para determinar os formatos que um aplicativo pode ler e gravar.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Chave do Registro de Conversão COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272090fb48b214daecd6350e6966350861366341fae055298a2fb2c90c9fb983
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993476"
---
# <a name="conversion"></a>Conversão

Usado pela caixa **de diálogo** Converter para determinar os formatos que um aplicativo pode ler e gravar.

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

As informações de conversão são usadas **pela caixa** de diálogo Converter para determinar quais formatos um aplicativo pode ler e gravar. Um formato de arquivo delimitado por vírgulas será indicado por um número se for um dos formatos da Área de Transferência definidos em Windows.h. Uma cadeia de caracteres indica que o formato não é definido em Windows.h (privado). Nesse caso, o formato acessível e que pode ser escrito é CF \_ OUTLINE (privado).

O *valor rformat* especifica o formato de arquivo que um aplicativo pode ler (converter).

O *valor rwformat* especifica o formato de arquivo que um aplicativo pode ler e gravar (ativar como).

 

 




