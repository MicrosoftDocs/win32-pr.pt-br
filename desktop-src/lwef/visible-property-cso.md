---
title: Propriedade Visible (objeto Commands)
description: Saiba mais sobre a Propriedade Visível do objeto Commands, que determina se a legenda da coleção Commands aparece no menu pop-up do caractere.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c742733d06f0a4c7ae2d10c7fb97a20e735b59370c61efa5f7204003f1cd81bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975466"
---
# <a name="visible-property-commands-object"></a>Propriedade Visible (objeto Commands)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define um valor que determina se a legenda da coleção [**Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Commands.Visible* *  \[  =  *boolean*\]



| Parte      | Descrição                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece no menu pop-up do caractere. <br/> **True** A legenda é exibida.<br/> **False** A legenda não é exibida.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Para que a legenda apareça no menu pop-up do caractere quando seu aplicativo não for o cliente de entrada ativa, essa propriedade deverá ser definida como **True** e a propriedade [**Legenda**](caption-property.md) definida para sua coleção comandos. Além disso, essa propriedade deve ser definida como **True** para que os comandos em sua coleção apareçam no menu pop-up quando seu aplicativo estiver ativo de entrada.

 

