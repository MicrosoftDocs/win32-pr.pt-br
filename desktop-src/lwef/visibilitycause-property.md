---
title: Propriedade VisibilityCause
description: Propriedade VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1e90b77dfdfae364761254676d0867a43aebacf516d4f2adad2973700d7e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398786"
---
# <a name="visibilitycause-property"></a>Propriedade VisibilityCause

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um valor inteiro que especifica o que causou o estado visível do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente* do. **Caracteres ("**_characterid_*_"). VisibilityCause_*



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


 

 




