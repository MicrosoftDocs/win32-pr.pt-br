---
title: BypassNegotiation
description: A chave do registro BypassNegotiation determina se as capacidades de negociação entre o servidor e o cliente ocorrem ou se as configurações pré-configuradas são usadas.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ba914b9c1ec1d5e3caef6b86ddbda49d021268e456c877ff4f67db86efd2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978246"
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

[Configurações de registro do EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




