---
title: VersionIndependentProgID
description: Associa um ProgID a um CLSID. Esse valor é usado para determinar a versão mais recente de um aplicativo de objeto.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006165"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgID

Associa um ProgID a um CLSID. Esse valor é usado para determinar a versão mais recente de um aplicativo de objeto.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz de reg** que especifica a versão mais recente do aplicativo de objeto.

O ProgID independente de versão é armazenado e mantido exclusivamente pelo código do aplicativo. Ao receber o ProgID independente de versão, a função [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retorna o CLSID da versão atual.

Você pode usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para converter entre essas duas representações.

 

 




