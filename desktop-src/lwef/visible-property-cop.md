---
title: Propriedade Visible (objeto Command)
description: Saiba mais sobre a Propriedade Visível do objeto Command, que retorna ou define se o Comando está visível no menu pop-up do caractere.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396241"
---
# <a name="visible-property-command-object"></a>Propriedade Visible (objeto Command)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define se [**o Comando**](/windows/desktop/lwef/the-command-object) está visível no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Commands(**"* name *"**). Booliana* *  \[  =  *visível*\]



| Parte      | Descrição                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se [**a**](/windows/desktop/lwef/the-command-object)legenda do Comando aparece no menu pop-up do caractere.<br/> **True** (Padrão) A legenda é exibida.<br/> **False** A legenda não é exibida.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

De definir essa propriedade como **False** quando você quiser incluir a entrada de voz para suas próprias interfaces sem que elas apareçam no menu pop-up do caractere. Se você definir [**uma**](/windows/desktop/lwef/the-command-object) propriedade Legenda do objeto Command como a cadeia de caracteres vazia (""), o texto da legenda [](visible-property.md) não aparecerá no menu pop-up (por exemplo, como uma linha em branco), independentemente da configuração de propriedade Visible. [](caption-property.md)

A [**configuração**](visible-property.md) de propriedade Visible da [**coleção de**](/windows/desktop/lwef/the-command-object) Comandos pai de um objeto [**Command**](/windows/desktop/lwef/the-commands-collection-object) não afeta a **configuração de** propriedade Visible do **Comando**.

 

