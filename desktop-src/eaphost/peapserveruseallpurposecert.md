---
title: PeapServerUseAllPurposeCert
description: A chave do registro PeapServerUseAllPurposeCert determina se os certificados de todas as finalidades são usados para autenticação PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104293624"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

A chave do registro PeapServerUseAllPurposeCert determina se os certificados de todas as finalidades são usados para autenticação PEAP.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** .



| Valor        | Descrição                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Os certificados de uso geral no repositório de certificados do cliente ou do servidor são selecionados para autenticação PEAP.     |
| Outros valores | Os certificados de uso insuficiente no repositório de certificados do cliente ou do servidor não são selecionados para autenticação PEAP. |



 

Se esse valor de registro não estiver presente, os certificados de uso máximo no repositório de certificados do cliente ou do servidor serão selecionados para autenticação PEAP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações do registro EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




