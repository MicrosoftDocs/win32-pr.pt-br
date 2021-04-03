---
title: Gravando clientes e servidores compatíveis com versões anteriores
description: Teoricamente, o esquema de controle de versão do RPC ajuda a impedir a comunicação inconsistente entre servidores e clientes modificados e seus correspondentes implantados.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, compatibilidade com versões anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084055"
---
# <a name="writing-backward-compatible-clients-and-servers"></a>Gravando clientes e servidores compatíveis com versões anteriores

Teoricamente, o esquema de controle de versão do RPC ajuda a impedir a comunicação inconsistente entre servidores e clientes modificados e seus correspondentes implantados. Na prática, no entanto, os desenvolvedores geralmente devem introduzir alterações em interfaces existentes sem modificar a versão, pois os clientes e servidores anteriores devem ser capazes de se comunicar com os novos. Esse é um problema maior para RPC padrão do que para COM; a consulta é uma maneira natural de procurar interfaces com suporte no COM, enquanto o tratamento de exceções de RPC deve ser usado para cobertura equivalente.

Esta seção aborda as melhores práticas de programação de RPC para tratar dessas situações. Esta seção é dividida nos seguintes tópicos:

-   [A teoria do controle de versão para RPC e COM](the-versioning-theory-for-rpc-and-com.md)
-   [Alterando interfaces de maneira compatível com versões anteriores](changing-interfaces-in-a-backward-compatible-manner.md)
-   [Exemplos de alterações incompatíveis](examples-of-incompatible-changes.md)

 

 




