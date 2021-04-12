---
title: Propriedade VisibilityCause
description: Propriedade VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364036"
---
# <a name="visibilitycause-property"></a>Propriedade VisibilityCause

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um valor inteiro que especifica o que causou o estado visível do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente* do. **Caracteres ("***characterid***"). VisibilityCause**



| Valor | Descrição                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | O caractere não foi mostrado.                                                                            |
| 1     | O usuário ocultou o caractere usando o comando no menu pop-up do ícone da barra de tarefas do caractere ou usando a entrada de fala. |
| 2     | O usuário mostrou o caractere.                                                                               |
| 3     | O aplicativo ocultou o caractere.                                                                          |
| 4     | Seu aplicativo mostrou o caractere.                                                                       |
| 5     | Outro aplicativo cliente ocultou o caractere.                                                                |
| 6     | Outro aplicativo cliente mostrou o caractere.                                                             |
| 7     | O usuário ocultou o caractere usando o comando no menu pop-up do caractere.                                 |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar essa propriedade para determinar o que causou o caractere a ser movido quando mais de um aplicativo estiver compartilhando (carregado) o mesmo caractere. Esses valores são os mesmos retornados pelos eventos [**show**](show-event.md) e [**Hide**](hide-event.md) .

## <a name="see-also"></a>Consulte Também

[**Ocultar evento**](hide-event.md), [**Mostrar evento**](show-event.md), [**ocultar método**](hide-method.md), [**Mostrar método**](show-method.md)


 

 




