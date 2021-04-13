---
title: AssumePhase2Fragmentation
description: A chave do registro AssumePhase2Fragmentation determina se o servidor e o cliente pressupõem a fragmentação da fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365329"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

A chave do registro AssumePhase2Fragmentation determina se o servidor e o cliente pressupõem a fragmentação da fase 2.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor   | Descrição                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | Servidor e cliente pressupõe que a outra parte não é capaz de fragmentação da fase 2 durante a autenticação de PEAP. |
| diferente | Servidor e cliente assumem que a outra parte é capaz de fragmentação da fase 2 durante a autenticação PEAP.     |



 

Se esse valor de registro não estiver presente, o servidor e o cliente assumem que a outra parte é capaz da fragmentação da fase 2 durante a autenticação de PEAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações do registro EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




