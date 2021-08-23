---
description: Referência de comando COPP
ms.assetid: b21db1cf-cac3-41d6-8189-6e01c8f91a7d
title: Referência de comando COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1a706863464b6f303e05cb88e28a075dffbfba7b6bf54f8289a2699e66a76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565966"
---
# <a name="copp-command-reference"></a>Referência de comando COPP

Esta seção descreve os comandos de COPP (protocolo de proteção de saída) certificados. Os comandos a seguir são definidos.



| Comando              | GUID                             |
|----------------------|----------------------------------|
| Definir nível de proteção | **COPPSetProtectionLevel de DXVA \_** |
| Definir sinalização        | **COPPSetSignaling de DXVA \_**       |



 

Comando definir nível de proteção

Define o nível de proteção para um mecanismo de proteção de saída especificado. Dependendo do conector, pode ser possível aplicar mais de um mecanismo de proteção no mesmo conector, com configurações diferentes para cada mecanismo.

**GUID**: DXVA \_ COPPSetProtectionLevel

**Dados de entrada**: uma estrutura de [**DXVA \_ COPPSetProtectionLevelCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetprotectionlevelcmddata) .

Definir comando de sinalização

Especifica informações sobre o sinal de vídeo diferente do nível de proteção.

Para o CGMS-A, determinados padrões de proteção exigem que o sinal televsion contenha informações sobre a taxa de proporção e outras informações nos mesmos pacotes VBI de forma de onda que os bits CGMS-A. As televisões podem exibir inadequadamente se as informações de taxa de proporção não estiverem consistentes com o fluxo de vídeo. O aplicativo pode usar esse comando para especificar a taxa de proporção para que o driver de gráficos possa gerar os pacotes VBI corretos.

Esse comando também é projetado para ser extensível se forem necessárias informações de sinal adicionais em padrões futuros.

**GUID**: DXVA \_ COPPSetSignaling

**Dados de entrada**: uma estrutura de [**DXVA \_ COPPSetSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppsetsignalingcmddata) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



