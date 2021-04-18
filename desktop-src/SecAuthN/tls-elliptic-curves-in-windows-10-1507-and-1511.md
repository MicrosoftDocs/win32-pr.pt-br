---
description: Curvas elípticas habilitadas nas versões 1507 e 1511 do Windows 10.
title: Curvas elípticas TLS no Windows 10 versão 1507 e 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814609"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a>Curvas elípticas TLS no Windows 10 versão 1507 e 1511

Para o Windows 10, versões 1507 e 1511, as seguintes curvas elípticas estão habilitadas e nesta ordem de prioridade por padrão usando o provedor Microsoft Schannel:

| Cadeia de curva elíptica | Disponível no modo FIPS |
|-------------|--------------|
| NistP256 | Yes |
| NistP384 | Yes |


As curvas elípticas a seguir têm suporte do provedor Microsoft Schannel, mas não habilitadas por padrão:

| Cadeia de curva elíptica | Disponível no modo FIPS |
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
- Para usar a política de grupo, [defina a ordem de curva ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) em configuração do computador > modelos administrativos > rede > definições de configuração SSL com a lista de prioridades para todas as curvas elípticas que você deseja habilitar.

- Para usar o PowerShell, consulte [cmdlets de TLS](/powershell/module/tls) para obter uma lista completa de sintaxe e descrições de cmdlets TLS.


> [!NOTE]
> Antes do Windows 10, as cadeias de caracteres do pacote de codificação foram anexadas com a curva elíptica para determinar a prioridade da curva. O Windows 10 dá suporte a uma configuração de ordem de prioridade de curva elíptica, portanto, o sufixo de curva elíptica não é necessário e é substituído pela nova ordem de prioridade de curva elíptica, quando fornecida, para permitir que as organizações usem a diretiva de grupo para configurar versões diferentes do Windows com os mesmos conjuntos de codificação.


## <a name="see-also"></a>Consulte Também

[Configurando a ordem de curva do TLS ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Gerenciando a ordem de ECC TLS](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Gerenciando as curvas do ECC do Windows usando Política de Grupo](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Cmdlets TLS](/powershell/module/tls)
