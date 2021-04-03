---
description: Se essa política do sistema por usuário estiver definida como &\# 0034; 1&\# 0034;, os usuários e administradores que executam uma instalação de manutenção de um produto serão impedidos de usar a caixa de diálogo de procura para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930084"
---
# <a name="disablemedia"></a>DisableMedia

Se essa [política do sistema](system-policy.md) por usuário for definida como "1", os usuários e administradores que executam uma instalação de manutenção de um produto serão impedidos de usar a caixa de diálogo de procura para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis. Procurar outros produtos é impedido, independentemente de a instalação ser feita com privilégios elevados. Ainda é possível que o usuário reinstale o produto da mídia se o usuário tiver uma origem de mídia rotulada corretamente.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Observe que a propriedade [**DISABLEMEDIA**](-disablemedia.md) tem um efeito diferente da política de DISABLEMEDIA. Definir a política do sistema DisableMedia, desabilita apenas a navegação para as fontes de mídia. Definir a propriedade **DISABLEMEDIA** impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto. No entanto, se a navegação estiver habilitada, um usuário ainda poderá navegar para uma fonte de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 



