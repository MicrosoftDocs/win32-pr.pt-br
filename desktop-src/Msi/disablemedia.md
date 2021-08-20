---
description: Se essa política de sistema por usuário estiver definida como &\# 0034;1&0034;, os usuários e administradores que executam uma instalação de manutenção de um produto serão impedidos de usar a caixa de diálogo Procurar para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos \# instaláveis.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2337a1698865b0b977e179021f6490e2fa651a8c4baa3a56e808d037926ad39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143242"
---
# <a name="disablemedia"></a>DisableMedia

Se essa política [](system-policy.md) de sistema por usuário estiver definida como "1", os usuários e administradores que executam uma instalação de manutenção de um produto serão impedidos de usar a caixa de diálogo Procurar para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis. A navegação por outros produtos é impedida, independentemente de a instalação ser feita com privilégios elevados. Ainda é possível que o usuário reinstale o produto da mídia se o usuário tiver uma fonte de mídia rotulada corretamente.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ atual de** \\ **políticas** de software \\  \\ do **usuário** \\  \\  Windows Microsoft

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Observe que a [**propriedade DISABLEMEDIA**](-disablemedia.md) tem um efeito diferente da política DisableMedia. Definir a política do sistema DisableMedia desabilita apenas a navegação para fontes de mídia. Definir a **propriedade DISABLEMEDIA** impede que o instalador registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto. No entanto, se a navegação estiver habilitada, um usuário ainda poderá navegar até uma fonte de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 



