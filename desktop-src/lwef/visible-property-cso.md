---
title: Propriedade Visible (objeto Commands)
description: Saiba mais sobre a Propriedade Visível do objeto Commands, que determina se a legenda da coleção Commands aparece no menu pop-up do caractere.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396251"
---
# <a name="visible-property-commands-object"></a>Propriedade Visible (objeto Commands)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

