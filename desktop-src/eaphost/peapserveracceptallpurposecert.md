---
title: PeapServerAcceptAllPurposeCert
description: A chave do registro PeapServerAcceptAllPurposeCert determina se os certificados de todas as finalidades são aceitos para a autenticação PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105789615"
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

[Configurações do registro EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




