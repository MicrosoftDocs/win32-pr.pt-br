---
description: O desafio de Microsoft Digest é gerado pela chamada inicial do servidor para a função AcceptSecurityContext (Digest).
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: Gerando o desafio de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a01a7edfa6498ed621e351c114e65a6d4ff6ef7a75b459cb29e00f0dc668a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623326"
---
# <a name="generating-the-digest-challenge"></a>Gerando o desafio de resumo

O desafio de Microsoft Digest é gerado pela chamada inicial do servidor para a função [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Essa chamada de função gera um nonce, que é um valor exclusivo que contém informações que podem ser usadas para detectar violações de segurança. Essa chamada também gera um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) parcial que é usado para manter informações de estado. Ao chamar **AcceptSecurityContext (Digest)** , você especifica sinalizadores de requisitos de contexto para controlar o comportamento de Microsoft Digest e para definir a qualidade de proteção. Para obter mais informações, consulte [Resumo de requisitos de contexto de desafio](#digest-challenge-context-requirements).

A saída da chamada inicial para a função [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) [](/windows/desktop/SecGloss/c-gly) é um buffer de segurança que contém um token que é enviado ao cliente com uma resposta HTTP 401 (acesso negado).

> [!Note]  
> Chamadas para [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) que não contêm informações nos buffers de entrada retornam um desafio de resumo.

 

## <a name="digest-challenge-context-requirements"></a>Requisitos de contexto de desafio Digest

Os requisitos de contexto são sinalizadores que determinam:

-   Se Microsoft Digest funciona como um mecanismo SASL ou protocolo de autenticação HTTP.
-   A qualidade de proteção com suporte do contexto de segurança compartilhado pelo cliente e servidor.

Por padrão, o Microsoft Digest funciona como um mecanismo SASL. Para usá-lo para autenticação HTTP, o \_ \_ sinalizador 0X10000000 (ASC req http) deve ser definido pelo servidor.

Os requisitos de contexto são especificados como sinalizadores passados para o parâmetro *fContextReq* da função [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Os sinalizadores afetam a qualidade de proteção do contexto de segurança, controlando a diretiva QoP no desafio.

Por padrão, a diretiva QoP é definida como "auth". Para gerar um desafio que define a diretiva QoP como "auth-int", o servidor deve especificar um ou mais dos seguintes sinalizadores:

-   \_integridade de req ASC \_
-   \_detecção de \_ Replay de req do ASC \_
-   \_detecção de \_ sequência de req do ASC \_

Somente para SASL: gere um desafio com a diretiva QoP definida como "auth-conf" especificando o sinalizador de \_ \_ requisito de contexto de confidencialidade de ASC. Como esse sinalizador não é válido para a autenticação HTTP, ele não pode ser usado com \_ o \_ sinalizador http ASC req.

Para obter mais informações sobre a diretiva QoP, consulte [qualidade de proteção e codificações](quality-of-protection-and-ciphers.md).

Para obter mais informações sobre os desafios, consulte [o conteúdo de um desafio de resumo](contents-of-a-digest-challenge.md).

 

 
