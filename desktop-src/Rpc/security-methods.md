---
title: Métodos de segurança
description: O Microsoft RPC dá suporte a dois métodos diferentes para adicionar segurança ao seu aplicativo distribuído.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005971"
---
# <a name="security-methods"></a>Métodos de segurança

O Microsoft RPC dá suporte a dois métodos diferentes para adicionar segurança ao seu aplicativo distribuído. O primeiro método é usar a interface de provedor de suporte de segurança (SSPI), que pode ser acessada usando as funções RPC. Em geral, é melhor usar esse método. O SSPI fornece os recursos de autenticação mais flexíveis e independentes de rede.

O segundo método é usar os recursos de segurança incorporados aos protocolos de transporte do sistema. O método de segurança no nível de transporte não é o método preferencial. Usar o SSPI é recomendado porque funciona em todos os transportes, entre plataformas, e fornece altos níveis de segurança, incluindo privacidade.

Esta seção fornece visões gerais de segurança de nível de transporte e SSPI nos seguintes tópicos:

-   [SSPI (interface do provedor de suporte de segurança)](security-support-provider-interface-sspi-.md)
-   [Segurança de transporte](transport-security.md)

 

 




