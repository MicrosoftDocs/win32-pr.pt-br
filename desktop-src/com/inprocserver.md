---
title: InprocServer
description: Especifica o caminho para a DLL do servidor em processo.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916259"
---
# <a name="inprocserver"></a>InprocServer

Especifica o caminho para a DLL do servidor em processo.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>Comentários

A entrada **InprocServer** é relativamente rara para classes insertáveis.

Atualmente, os servidores em processo são registrados usando a entrada de registro **InprocServer** . Os servidores em processo de 32 bits e 64 bits devem usar a entrada [**InprocServer32**](inprocserver32.md) . Se um contêiner estiver pesquisando o registro de um servidor em processo, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits tem prioridade com um contêiner de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




