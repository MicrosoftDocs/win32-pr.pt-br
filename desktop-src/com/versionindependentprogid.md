---
title: VersionIndependentProgID
description: Associa um ProgID a um CLSID. Esse valor é usado para determinar a versão mais recente de um aplicativo de objeto.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- Chave do Registro VersionIndependentProgID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe1defaa52df5251d6c021655d6e84c90677e2a2d57f0bfb67f925e0ffa5bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549712"
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

Esse é um **valor \_ REG SZ** que especifica a versão mais recente do aplicativo de objeto.

O ProgID independente de versão é armazenado e mantido exclusivamente pelo código do aplicativo. Quando dada a ProgID independente de versão, a [**função CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retorna o CLSID da versão atual.

Você pode usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para converter entre essas duas representações.

 

 




