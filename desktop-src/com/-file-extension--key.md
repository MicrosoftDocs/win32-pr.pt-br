---
title: Chave de file_extension
description: Associa uma extensão de nome de arquivo a um ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823015"
---
# <a name="file_extension-key"></a>Chave de> de <de extensão de arquivo \_

Associa uma extensão de nome de arquivo a um ProgID.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>Comentários

As informações contidas na chave de extensão de nome de arquivo são usadas pelo Windows Explorer e pelos monikers de arquivo. [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa a chave de extensão de nome de arquivo para fornecer o CLSID associado.

A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Talvez**](filetype-key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




