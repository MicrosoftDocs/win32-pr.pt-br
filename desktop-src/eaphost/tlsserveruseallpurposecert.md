---
title: TlsServerUseAllPurposeCert
description: A chave do registro TlsServerUseAllPurposeCert determina se os certificados de todas as finalidades são usados para autenticação EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2f9d47b4e80409c27c71fe3655a1d3266571e0f8a8dd757e5334b0ef9fec40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085691"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

A chave do registro TlsServerUseAllPurposeCert determina se os certificados de todas as finalidades são usados para autenticação EAP-TLS.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor        | Descrição                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Os certificados de uso geral no repositório de certificados do cliente ou do servidor são selecionados para autenticação PEAP.     |
| Outros valores | Os certificados de uso insuficiente no repositório de certificados do cliente ou do servidor não são selecionados para autenticação PEAP. |



 

Se esse valor de registro não estiver presente, os certificados de uso máximo no repositório de certificados do cliente ou do servidor serão selecionados para autenticação EAP-TLS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações de registro do EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




