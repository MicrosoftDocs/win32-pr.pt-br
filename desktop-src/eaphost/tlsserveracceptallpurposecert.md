---
title: TlsServerAcceptAllPurposeCert
description: A chave do registro TlsServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para autenticação EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105749183"
---
# <a name="tlsserveracceptallpurposecert"></a>TlsServerAcceptAllPurposeCert

A chave do registro TlsServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para autenticação EAP-TLS.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor        | Descrição                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | O servidor e o cliente aceitam certificados com todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS.       |
| Outros valores | O servidor e o cliente não aceitam certificados de todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS |



 

Se esse valor de registro não estiver presente, o servidor e o cliente aceitarão os certificados de todas as finalidades enviadas pela outra entidade para autenticação EAP-TLS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações do registro EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




