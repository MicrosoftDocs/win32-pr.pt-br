---
description: A qualidade de proteção, identificada pela diretiva QoP, é especificada pela primeira vez pelo servidor no desafio de resumo e, em seguida, confirmada pelo cliente na resposta de desafio.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualidade da proteção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202acbf319601af74efc35117990f27cc6edff76f27da243453f82bf50984977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920445"
---
# <a name="quality-of-protection"></a>Qualidade da proteção

A qualidade de proteção, identificada pela diretiva QoP, é especificada pela primeira vez pelo servidor no desafio de resumo e, em seguida, confirmada pelo cliente na resposta de desafio. Se o cliente exigir uma qualidade de proteção para a qual o servidor não oferece suporte, o cliente deverá encerrar a autenticação.

Os valores possíveis para a diretiva QoP são descritos na tabela a seguir.



| Valor                   | Descrição                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| propósito                  | Somente autenticação.                                                                                                                         |
| "auth-int"              | Verificação de [*integridade*](../secgloss/i-gly.md) e autenticação usando assinaturas.                  |
| (SASL somente) "auth-conf" | Autenticação, integridade e verificação de confidencialidade usando assinaturas e criptografia. Para obter mais informações, consulte [codificações](ciphers.md). |



 

A qualidade da proteção é determinada pelos sinalizadores de requisitos de contexto passados para o Microsoft Digest SSP. A tabela a seguir lista os sinalizadores relacionados à qualidade de proteção e o valor resultante da diretiva QoP.



| Sinalizador                         | valor de QoP               |
|------------------------------|-------------------------|
| *Xxx* \_ confidencialidade de REQ. \_  | "auth-conf" (SASL somente) |
| *Xxx* \_ detecção de repetição do REQ. \_ \_   | "auth-int"              |
| *Xxx* \_ \_detecção de sequência de req \_ | "auth-int"              |
| *Xxx* \_ integridade de REQ. \_        | "auth-int"              |
| (nenhum)                       | propósito                  |



 

> [!Note]  
> Os sinalizadores de requisitos de contexto especificados por aplicativos de servidor têm um prefixo de ASC, e os especificados pelos clientes são prefixados com a ISC. Para determinar os valores de sinalizador usados pelo seu aplicativo, substitua um destes prefixos por *xxx*.

 

Para obter informações adicionais relacionadas ao servidor, consulte [gerando o desafio Digest](generating-the-digest-challenge.md).

Para obter informações adicionais relacionadas ao cliente, consulte [gerando a resposta de desafio de resumo](generating-the-digest-challenge-response.md).

 

 
