---
title: ProxyStubClsid
description: Mapas um IID para um CLSID em DLLs de proxy de 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valor do Registro ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f86db768979a72d2d2f0b8c7a137d6b105f4a52d082ec50c6e78ba271fbca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129988"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Mapas um IID para um CLSID em DLLs de proxy de 16 bits.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG SZ** que especifica o CLSID para o IID.

Se você adicionar interfaces, deverá usar essa entrada para registrá-las (sistemas de 16 bits) para que o OLE possa encontrar o código de comunicação removível apropriado para estabelecer a comunicação entre processos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




