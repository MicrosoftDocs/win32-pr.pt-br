---
description: O SSP do Schannel implementa versões dos protocolos TLS, DTLS e SSL. versões diferentes do Windows dão suporte a versões de protocolo diferentes.
ms.assetid: FF716A4E-ABF2-4773-9588-9D200945A866
title: Protocolos em TLS/SSL (SSP Schannel)
ms.topic: article
ms.date: 01/20/2021
ms.custom: contperf-fy21q3
ms.openlocfilehash: 0aa3c3900a422a1460a2163043fb736e590ca2fe
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436261"
---
# <a name="protocols-in-tlsssl-schannel-ssp"></a>Protocolos em TLS/SSL (SSP Schannel)

O SSP do Schannel implementa versões dos protocolos TLS, DTLS e SSL. versões diferentes do Windows dão suporte a versões de protocolo diferentes.

## <a name="tls-protocol-version-support"></a>Suporte à versão do protocolo TLS

A tabela a seguir exibe o suporte ao provedor Microsoft Schannel de versões do protocolo TLS.

> [!TIP]
> Talvez seja necessário rolar horizontalmente para exibir todas as colunas na tabela.

| Sistema operacional Windows | Cliente TLS 1,0 | Servidor TLS 1,0 | Cliente TLS 1,1 | Servidor TLS 1,1 | Cliente TLS 1,2 | Servidor TLS 1,2 | Cliente TLS 1,3 | Servidor TLS 1,3 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Windows Vista/Windows Server 2008                     | habilitado        | habilitado        | Sem suporte  | Sem suporte  | Sem suporte  | Sem suporte  | Sem suporte  | Sem suporte  |
| Windows Server 2008 com Service Pack 2 (SP2)         | habilitado        | habilitado        | Desabilitado       | Desabilitado       | Desabilitado       | Desabilitado       | Sem suporte  | Sem suporte  |
| Windows 7/Windows Server 2008 R2                      | habilitado        | habilitado        | Desabilitado       | Desabilitado       | Desabilitado       | Desabilitado       | Sem suporte  | Sem suporte  |
| Windows 8/Windows Server 2012                         | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 8.1/Windows Server 2012 R2                    | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1507                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1511                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1607/Windows Server 2016 Standard | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1703                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1709                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1803                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1809//Windows Server 2019         | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1903                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 1909                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 2004                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 20H2                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows 10, versão 21H1                              | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | Sem suporte  | Sem suporte  |
| Windows Server 2022                                   | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        | habilitado        |


## <a name="dtls-protocol-version-support"></a>Suporte à versão do protocolo DTLS

O exemplo a seguir lista o suporte do Provedor Schannel da Microsoft de versões de protocolo DTLS.

*Dica: talvez seja necessário rolar horizontalmente para exibir todas as colunas nesta tabela:*

| Sistema operacional Windows                                            | Cliente DTLS 1.0 | Servidor DTLS 1.0 | Cliente DTLS 1.2 | Servidor DTLS 1.2 |
|-------------------------------------------------------|-----------------|-----------------|-----------------|-----------------|
| Windows Vista/Windows Server 2008                     | Sem suporte   | Sem suporte   | Sem suporte   | Sem suporte   |
| Windows Server 2008 com SP2                          | Sem suporte   | Sem suporte   | Sem suporte   | Sem suporte   |
| Windows 7/Windows Server 2008 R2                      | habilitado         | habilitado         | Sem suporte   | Sem suporte   |
| Windows 8/Windows Server 2012                         | habilitado         | habilitado         | Sem suporte   | Sem suporte   |
| Windows 8.1/Windows Server 2012 R2                    | habilitado         | habilitado         | Sem suporte   | Sem suporte   |
| Windows 10, versão 1507                              | habilitado         | habilitado         | Sem suporte   | Sem suporte   |
| Windows 10, versão 1511                              | habilitado         | habilitado         | Sem suporte   | Sem suporte   |
| Windows 10, versão 1607/Windows Server 2016 Standard | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versão 1703                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versão 1803                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versão 1809                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versão 1903                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versão 1909                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versão 2004                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versão 20H2                              | habilitado         | habilitado         | habilitado         | habilitado         |
| Windows 10, versão 21H1                              | habilitado         | habilitado         | habilitado         | habilitado         |

## <a name="pre-tls-standard-protocols-support"></a>Suporte a protocolos padrão pré-TLS

Veja a seguir a lista de suporte do Provedor Schannel da Microsoft de protocolos padrão pré-TLS:

*Dica: talvez seja necessário rolar horizontalmente para exibir todas as colunas nesta tabela:*

| Sistema operacional Windows                                            | PCT 1.0       | Cliente SSL2   | Servidor SSL2   | Cliente SSL3 | Servidor SSL3 |
|-------------------------------------------------------|---------------|---------------|---------------|-------------|-------------|
| Windows Vista/Windows Server 2008                     | Sem suporte | Desabilitado      | habilitado       | habilitado     | habilitado     |
| Windows Server 2008 com SP2                          | Sem suporte | Desabilitado      | habilitado       | habilitado     | habilitado     |
| Windows 7/Windows Server 2008 R2                      | Sem suporte | Desabilitado      | habilitado       | habilitado     | habilitado     |
| Windows 8/Windows Server 2012                         | Sem suporte | Desabilitado      | Desabilitado      | habilitado     | habilitado     |
| Windows 8.1/Windows Server 2012 R2                    | Sem suporte | Desabilitado      | Desabilitado      | habilitado     | habilitado     |
| Windows 10, versão 1507                              | Sem suporte | Desabilitado      | Desabilitado      | habilitado     | habilitado     |
| Windows 10, versão 1511                              | Sem suporte | Desabilitado      | Desabilitado      | habilitado     | habilitado     |
| Windows 10, versão 1607/Windows Server 2016 Standard | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |
| Windows 10, versão 1703                              | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |
| Windows 10, versão 1803                              | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |
| Windows 10, versão 1809                              | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |
| Windows 10, versão 1903                              | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |
| Windows 10, versão 1909                              | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |
| Windows 10, versão 2004                              | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |
| Windows 10, versão 20H2                              | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |
| Windows 10, versão 21H1                              | Sem suporte | Sem suporte | Sem suporte | Desabilitado    | Desabilitado    |


> [!IMPORTANT]
> A partir Windows 10, versão 1607 e Windows Server 2016, o SSL 2.0 foi removido e não tem mais suporte.

> [!TIP]  
> Todas as versões Windows aceitarão uma mensagem de formato unificado "ClientHello" mesmo quando a versão 2 do SSL estiver desabilitada ou não for mais suportada.
