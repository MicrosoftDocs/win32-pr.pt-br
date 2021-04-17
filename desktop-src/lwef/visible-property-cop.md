---
title: Propriedade Visible (objeto Command)
description: Propriedade Visible
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105811735"
---
# <a name="visible-property-command-object"></a>Propriedade Visible (objeto Command)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

