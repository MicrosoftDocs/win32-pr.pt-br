---
title: ProxyStubClsid32
description: Mapeia um IID para um CLSID em DLLs de proxy de 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- COM valor do registro ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294533"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Mapeia um IID para um CLSID em DLLs de proxy de 32 bits.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Comentários

Este é um **valor \_ sz de reg** que especifica o CLSID para o IID.

Essa é uma entrada necessária, pois o mapeamento de IID para CLSID pode ser diferente para interfaces de 16 bits e de 32 bits. O mapeamento de IID para CLSID depende da maneira como os proxies de interface são empacotados em um conjunto de DLLs de proxy.

Se você adicionar interfaces, deverá usar essa entrada para registrá-las (sistemas de 32 bits) para que o OLE possa encontrar o código de comunicação remota apropriado para estabelecer a comunicação entre processos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Interface**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 