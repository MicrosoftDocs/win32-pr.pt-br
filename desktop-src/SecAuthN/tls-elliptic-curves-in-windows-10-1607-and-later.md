---
description: Curvas elípticas habilitadas Windows 10 versão 1607 e posteriores.
title: Curvas elípticas do TLS Windows 10 versão 1607 e posterior
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 237d0f7a7b4b2a7fecb99a91f21c55349e7d435b221e1b3297afd1ba614cc92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915841"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a>Curvas elípticas do TLS Windows 10 versão 1607 e posterior

Por Windows 10, versões 1607 e posteriores, as seguintes curvas elípticas são habilitadas e, nessa ordem de prioridade, por padrão, usando o Provedor Schannel da Microsoft:

| Cadeia de caracteres de curva elíptica | Disponível no modo FIPS |
|-------------|--------------|
| curve25519 | No |
| NistP256 | Yes |
| NistP384 | Yes |


As seguintes curvas elípticas são suportadas pelo Provedor Schannel da Microsoft, mas não habilitadas por padrão:

| Cadeia de caracteres de curva elíptica | Disponível no modo FIPS |
|-------------|--------------|
| brainpoolP256r1 | No |
| brainpoolP384r1 | No |
| brainpoolP512r1 | No |
| nistP192 | No |
| nistP224 | No |
| nistP521 | Yes |
| secP160k1 | No |
| secP160r1 | No |
| secP160r2 | No |
| secP192k1 | No |
| secP192r1 | No |
| secP224k1 | No |
| secP224r1 | No |
| secP256k1 | No |
| secP256r1 | No |
| secP384r1 | No |
| secP521r1 | No |



## <a name="enabling-elliptic-curves"></a>Habilitando curvas elípticas

Para adicionar curvas elípticas, implante uma política de grupo ou use os cmdlets TLS:
- Para usar a política de grupo, configure a Ordem de Curva [ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) em Configuração do Computador > Modelos Administrativos > Network > Configuração SSL Configurações com a lista de prioridade para todas as curvas elípticas que você deseja habilitar.

- Para usar o PowerShell, consulte [Cmdlets TLS](/powershell/module/tls) para ver uma lista completa de sintaxe e descrições do cmdlet TLS.


> [!NOTE]
> Antes de Windows 10, as cadeias de caracteres do conjunto de criptografias eram anexadas com a curva elíptica para determinar a prioridade da curva. Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica para que o sufixo de curva elíptica não seja necessário e seja substituído pela nova ordem de prioridade de curva elíptica, quando fornecido, para permitir que as organizações usem a política de grupo para configurar diferentes versões do Windows com os mesmos suites de criptografia.


## <a name="see-also"></a>Consulte Também

[Configurando a ordem de curva TLS ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Gerenciando a ordem ECC do TLS](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Gerenciando Windows curvas ECC usando Política de Grupo](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Cmdlets TLS](/powershell/module/tls)
