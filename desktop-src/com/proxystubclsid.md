---
title: ProxyStubClsid
description: Mapeia um IID para um CLSID em DLLs de proxy de 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- COM valor do registro ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005923"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Mapeia um IID para um CLSID em DLLs de proxy de 16 bits.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Comentários

Este é um **valor \_ sz de reg** que especifica o CLSID para o IID.

Se você adicionar interfaces, deverá usar essa entrada para registrá-las (sistemas de 16 bits) para que o OLE possa encontrar o código de comunicação remota apropriado para estabelecer a comunicação entre processos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




