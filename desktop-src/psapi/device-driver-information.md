---
title: Informações de driver de dispositivo
description: Drivers de dispositivo e módulos são semelhantes porque ambos são baseados em arquivos PE.
ms.assetid: 4f4ec15b-5592-4fe3-b754-fda25ab24159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0735e791b8c6e1fc7434decc7ac71ccb5c1c469e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005142"
---
# <a name="device-driver-information"></a>Informações de driver de dispositivo

Drivers de dispositivo e módulos são semelhantes porque ambos são baseados em arquivos PE. No entanto, embora cada processo tenha sua própria lista privada de módulos carregados, os drivers de dispositivo têm módulos que são globais para o sistema. Portanto, o PSAPI tem funções específicas para obter a lista de drivers de dispositivo e seus nomes.

Você pode recuperar o endereço de carregamento para cada driver de dispositivo chamando a função [**EnumDeviceDrivers**](/windows/desktop/api/Psapi/nf-psapi-enumdevicedrivers) . Essa função preenche uma matriz de valores **LPVOID** com os endereços de carga de todos os drivers de dispositivo no sistema.

A função [**GetDeviceDriverBaseName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverbasenamea) usa um endereço de carregamento de driver como entrada e preenche um buffer com o nome base do driver (por exemplo, Win32k.sys). Uma função relacionada, [**GetDeviceDriverFileName**](/windows/desktop/api/Psapi/nf-psapi-getdevicedriverfilenamea), usa os mesmos parâmetros e retorna o caminho para o driver de dispositivo (por exemplo, C: \\ Windows \\ System32 \\Win32k.sys).

 

 




