---
title: PeapServerUseAllPurposeCert
description: A chave do Registro PeapServerUseAllPurposeCert determina se os certificados de todos os fins são usados para autenticação PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5086a0067bab70a0e222def34d1adf236b37127c0d1ff6c91ac83b8b28c73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042814"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

A chave do Registro PeapServerUseAllPurposeCert determina se os certificados de todos os fins são usados para autenticação PEAP.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG DWORD.**



| Valor        | Descrição                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Certificados de uso único no armazenamento de certificados do cliente ou do servidor são selecionados para autenticação PEAP.     |
| Outros valores | Certificados de uso único no armazenamento de certificados do cliente ou do servidor não são selecionados para autenticação PEAP. |



 

Se esse valor do Registro não estiver presente, os certificados de uso total no armazenamento de certificados do cliente ou do servidor serão selecionados para autenticação PEAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro EAPHost Configurações](eaphost-registry-settings.md)
</dt> </dl>

 

 




