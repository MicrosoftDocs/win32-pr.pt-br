---
title: InprocServer
description: Especifica o caminho para a DLL do servidor em processo.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6cd1c7ab32733687292f01ddb48167c68243c62345fb17af3b6533a5cb454d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029886"
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

 

 




