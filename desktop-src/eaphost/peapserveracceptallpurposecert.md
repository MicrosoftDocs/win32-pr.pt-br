---
title: PeapServerAcceptAllPurposeCert
description: A chave do registro PeapServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para a autenticação PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d568ef2cf3e7fd5eeeaa650e5e6e4fd32a8e1c8d6baa0ed91434a5c0aa60ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784678"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

A chave do registro PeapServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para a autenticação PEAP.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor        | Descrição                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | O servidor e o cliente aceitam certificados com todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS.       |
| Outros valores | O servidor e o cliente não aceitam certificados de todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS |



 

Se esse valor de registro não estiver presente, o servidor e o cliente aceitarão os certificados de todas as finalidades enviadas pela outra entidade para autenticação de PEAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações de registro do EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




