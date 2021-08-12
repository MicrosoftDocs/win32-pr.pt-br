---
description: Propriedade de contexto de segurança
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Propriedade de contexto de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c537dc8c9b925fff5f7fc4f3da99fd361bfb02f61008b7d7af8a421b9f1d11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546817"
---
# <a name="security-context-property"></a>Propriedade de contexto de segurança

Assim como ocorre com cada serviço automático fornecido pelo COM+, a verificação automática de função baseia-se nas propriedades incluídas no contexto do objeto. A determinação de se uma verificação de segurança deve ser executada em uma chamada em um componente é baseada na propriedade de segurança no contexto de objeto criado quando o componente configurado é instanciado.

Geralmente, você não precisa se preocupar com essa propriedade; Ele é usado diretamente pelo COM+, não por você. No entanto, em algumas circunstâncias, talvez você queira um controle estrito sobre a ativação de um objeto. Nesse caso, a propriedade de segurança pode afetar em qual contexto seu objeto é ativado. Ou seja, se um objeto tiver uma configuração incompatível com o contexto de seu criador, ele será ativado em seu próprio contexto. A propriedade de segurança pode influenciar isso, assim como qualquer propriedade no contexto do objeto.

Se não quiser que as configurações de segurança influenciem a ativação, você poderá escolher somente a verificação de acesso no nível de processo. Isso suprime a propriedade Security no contexto do objeto, embora efetivamente desabilite a verificação baseada em função e torne [as informações de contexto de chamada de segurança](security-call-context-information.md) indisponíveis.

Para obter mais informações sobre verificações de acesso no nível do processo, consulte [limites de segurança](security-boundaries.md). Para ver como definir a segurança em nível de processo, consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).

Para obter mais informações sobre o contexto de objeto, consulte [contextos](com--contexts.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando funções com eficiência](designing-roles-effectively.md)
</dt> <dt>

[Limites de segurança](security-boundaries.md)
</dt> <dt>

[Informações de contexto de chamada de segurança](security-call-context-information.md)
</dt> <dt>

[Usando funções para autorização de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



