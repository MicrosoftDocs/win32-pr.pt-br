---
description: A função QueryContextAttributes (Digest) fornece informações sobre as configurações atuais de um contexto de segurança.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Consultando atributos de contexto de segurança de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24499d5119814edec12f29cf5a39ea027f95c100626be1af1d132c952682599c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919955"
---
# <a name="querying-digest-security-context-attributes"></a>Consultando atributos de contexto de segurança de resumo

A função [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) fornece informações sobre as configurações atuais de um [*contexto de segurança*](../secgloss/s-gly.md).

Microsoft Digest dá suporte à consulta dos seguintes atributos de contexto de segurança.



| Atributo                   | Descrição                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_informações da \_ chave \_ attr SECPKG     | Informações relacionadas aos algoritmos de assinatura e criptografia em uso.                                                                                                                                   |
| \_informações do \_ pacote \_ attr SECPKG | Informações gerais referentes a Microsoft Digest, como o tamanho máximo de token permitido pelo [*pacote de segurança*](../secgloss/s-gly.md). |
| \_tamanhos de attr SECPKG \_         | Os tamanhos máximos permitidos para dados relacionados à mensagem, como assinaturas.                                                                                                                                |



 

 

 
