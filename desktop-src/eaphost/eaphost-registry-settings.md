---
title: Configurações do registro EAPHost
description: Os valores do registro nas chaves do registro a seguir controlam aspectos da funcionalidade do EAPHost.
ms.assetid: 2b954911-7c2e-4c86-b031-24632235a669
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e4d258062ee2ae365924ecda22c2660ed5b742
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103823482"
---
# <a name="eaphost-registry-settings"></a>Configurações do registro EAPHost

Os valores do registro nas chaves do registro a seguir controlam aspectos da funcionalidade do EAPHost.



| Subchave                                                                 | Description                                                                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BypassNegotiation](bypassnegotiation.md)                             | Determina se a negociação de recursos entre o servidor RAS e o cliente ocorre.<br/>                                                                              |
| [AssumePhase2Fragmentation](assumephase2fragmentation.md)             | Determina se o servidor RAS e o cliente pressupõem a fragmentação da fase 2.<br/>                                                                                         |
| [OverrideEAPCertificateSelection](overrideeapcertificateselection.md) | Determina se o cliente substituirá o comportamento de seleção de certificado de cartão inteligente padrão e fornecerá a um usuário mais certificados para sua escolha.<br/> |
| [PeapServerUseAllPurposeCert](peapserveruseallpurposecert.md)         | Determina se os certificados de todas as finalidades são usados para autenticação PEAP.<br/>                                                                                      |
| [PeapServerAcceptAllPurposeCert](peapserveracceptallpurposecert.md)   | Determina se os certificados de todas as finalidades são aceitos para autenticação PEAP.<br/>                                                                                  |
| [TlsServerUseAllPurposeCert](tlsserveruseallpurposecert.md)           | Determina se os certificados de todas as finalidades são usados para autenticação EAP-TLS.<br/>                                                                                   |
| [TlsServerAcceptAllPurposeCert](tlsserveracceptallpurposecert.md)     | Determina se os certificados de todas as finalidades são aceitos para autenticação EAP-TLS.<br/>                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência da API EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 





