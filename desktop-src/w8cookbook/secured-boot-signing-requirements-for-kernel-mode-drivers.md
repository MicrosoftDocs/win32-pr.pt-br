---
title: Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel
description: Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6593df6707dc26b36fceca796c436ed45f3f0c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885063"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel

## <a name="platforms"></a>Plataformas

**clientes** – Windows 8  
**servidores** – Windows Server 2012  


## <a name="description"></a>Description

em Windows 8 e Windows Server 2012, incluindo o WinPE, o kernel foi bloqueado para evitar que o malware introduzido pelos kits de inicialização ou raiz evite burlar Windows requisitos de segurança do sistema operacional para drivers assinados.

Essa alteração afeta todos os drivers de modo kernel para dispositivos que dão suporte à inicialização segura da UEFI (Unified Extensible Firmware Interface); a inicialização segura de UEFI é necessária para a certificação Windows 8 para computadores cliente e opcional para servidores. Ele não afeta os drivers do modo de usuário.

O desenvolvimento padrão para drivers de modo kernel envolve o uso de depuração de modo kernel ou da configuração testsigning de dados de configuração de inicialização (BCD) &lt; &gt; . Ambos são desabilitados quando a inicialização segura está ativada.

## <a name="manifestation"></a>Manifestação

Os drivers do modo kernel não serão executados se não forem assinados corretamente por uma autoridade de certificação (CA) confiável. O sistema operacional não permitirá que drivers não confiáveis sejam executados e mecanismos padrão, como depuração de kernel e testsigning, não sejam permitidos.

## <a name="mitigation"></a>Atenuação

Para testar os drivers, você deve desabilitar a inicialização segura no BIOS, bem como atender aos outros requisitos de assinatura de teste (veja abaixo).

Ao distribuir drivers mais amplamente eles devem ser assinados corretamente por uma AC confiável.

## <a name="resources"></a>Recursos

-   [Drivers de assinatura](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 
