---
title: AssumePhase2Fragmentation
description: A chave do Registro AssumePhase2Fragmentation determina se o servidor e o cliente assumem a fragmentação da fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caee785b0c89b92aaf4b01c590425c451b9a977664e915874e7eb5ad1edf46aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275833"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

A chave do Registro AssumePhase2Fragmentation determina se o servidor e o cliente assumem a fragmentação da fase 2.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG DWORD.**



| Valor   | Descrição                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | O servidor e o cliente supõem que a outra parte não é capaz de fragmentação da fase 2 durante a autenticação PEAP. |
| Zero | O servidor e o cliente supõem que a outra parte é capaz de fragmentação da fase 2 durante a autenticação PEAP.     |



 

Se esse valor do Registro não estiver presente, o servidor e o cliente presumirão que a outra parte é capaz de fragmentar a fase 2 durante a autenticação PEAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro EAPHost Configurações](eaphost-registry-settings.md)
</dt> </dl>

 

 




