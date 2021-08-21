---
title: ProxyStubClsid32
description: Mapas um IID para um CLSID em DLLs de proxy de 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valor do Registro ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9098ffc7771d3f900489292694ade462a2214e733294a1ed18e6ddb9817692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309892"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Mapas um IID para um CLSID em DLLs de proxy de 32 bits.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG SZ** que especifica o CLSID para o IID.

Essa é uma entrada necessária, pois o mapeamento IID para CLSID pode ser diferente para interfaces de 16 bits e 32 bits. O mapeamento de IID para CLSID depende da maneira como os proxies de interface são empacotados em um conjunto de DLLs de proxy.

Se você adicionar interfaces, deverá usar essa entrada para registrá-las (sistemas de 32 bits) para que o OLE possa encontrar o código de comunicação de comunicação comunicação removível apropriado para estabelecer a comunicação entre processos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Imarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Interface**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 