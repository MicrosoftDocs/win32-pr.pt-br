---
title: Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel
description: Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105765783"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

No Windows 8 e no Windows Server 2012, incluindo o WinPE, o kernel foi bloqueado para evitar que malwares introduzidos por kits de inicialização ou raiz contornem os requisitos de segurança do sistema operacional Windows para drivers assinados.

Essa alteração afeta todos os drivers de modo kernel para dispositivos que dão suporte à inicialização segura da UEFI (Unified Extensible Firmware Interface); A inicialização segura de UEFI é necessária para a certificação do Windows 8 para computadores cliente e opcional para servidores. Ele não afeta os drivers do modo de usuário.

O desenvolvimento padrão para drivers de modo kernel envolve o uso de depuração de modo kernel ou da configuração BCD (dados de configuração de inicialização) <testsigning> . Ambos são desabilitados quando a inicialização segura está ativada.

## <a name="manifestation"></a>Manifestação

Os drivers do modo kernel não serão executados se não forem assinados corretamente por uma autoridade de certificação (CA) confiável. O sistema operacional não permitirá que drivers não confiáveis sejam executados e mecanismos padrão, como depuração de kernel e testsigning, não sejam permitidos.

## <a name="mitigation"></a>Atenuação

Para testar os drivers, você deve desabilitar a inicialização segura no BIOS, bem como atender aos outros requisitos de assinatura de teste (veja abaixo).

Ao distribuir drivers mais amplamente eles devem ser assinados corretamente por uma AC confiável.

## <a name="resources"></a>Recursos

-   [Drivers de assinatura](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 