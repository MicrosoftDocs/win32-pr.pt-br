---
title: Propriedade Visible (objeto Command)
description: Saiba mais sobre a propriedade Visible do objeto Command, que retorna ou define se o comando está visível no menu pop-up do caractere.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ebc5dee52ff3ab388674bd844e476f0bcc768595b1ba5e69d3c3be5435553f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975456"
---
# <a name="visible-property-command-object"></a>Propriedade Visible (objeto Command)

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define se o [**comando**](/windows/desktop/lwef/the-command-object) está visível no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*Agente ***. Caracteres (**"* characterid *"**). Comandos (**"* name *" * *).* *  \[  =  *Booliano* visível\]



| Parte      | Descrição                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se a legenda do [**comando**](/windows/desktop/lwef/the-command-object)aparece no menu pop-up do caractere.<br/> **True** (padrão) a legenda é exibida.<br/> **Falso** A legenda não aparece.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Defina essa propriedade como **false** quando desejar incluir entrada de voz para suas próprias interfaces sem que elas apareçam no menu pop-up para o caractere. Se você definir a propriedade [**legenda**](caption-property.md) de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) como a cadeia de caracteres vazia (""), o texto da legenda não será exibido no menu pop-up (por exemplo, como uma linha em branco), independentemente da configuração da propriedade [**visível**](visible-property.md) .

A configuração da propriedade [**Visible**](visible-property.md) da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) pai de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) não afeta a configuração da propriedade **visível** do **comando**.

 

