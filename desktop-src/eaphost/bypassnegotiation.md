---
title: BypassNegotiation
description: A chave do registro BypassNegotiation determina se as capacidades de negociação entre o servidor e o cliente ocorrem ou se as configurações pré-configuradas são usadas.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365347"
---
# <a name="bypassnegotiation"></a>BypassNegotiation

A chave do registro BypassNegotiation determina se as capacidades de negociação entre o servidor e o cliente ocorrem ou se as configurações pré-configuradas são usadas.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor   | Descrição                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | Servidor e cliente negociam recursos EAP.                                                                                                                                                        |
| diferente | O servidor e o cliente não negociam os recursos EAP. Servidor e cliente usam o valor da chave do registro [AssumePhase2Fragmentation](assumephase2fragmentation.md) para encontrar os recursos da outra parte. |



 

Se esse valor de registro não estiver presente, o servidor e o cliente negociarão os recursos EAP..

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações do registro EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




