---
title: Propriedade Caption (objeto de coleção commands)
description: Saiba mais sobre a propriedade Caption do objeto Coleção de Comandos. O Microsoft Agent foi preterido a partir Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3467543de127bf0d9e898273f68d4cb921b7ab88ef52e965d73be4c1b465786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976696"
---
# <a name="caption-property-commands-collection-object"></a>Propriedade Caption (objeto de coleção commands)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Determina o texto exibido para um [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_")._ * [Cadeia de caracteres Commands.Caption](caption-property.md) \[  =  \]



| Parte     | Descrição                                                              |
|----------|--------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada para o texto exibido como a legenda. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Definir a propriedade [**Legenda**](caption-property.md) para sua coleção [**De**](/windows/desktop/lwef/the-commands-collection-object) comandos define como ela será exibida no menu pop-up do caractere quando sua propriedade [**Visible**](visible-property.md) estiver definida como True e seu aplicativo não for o cliente ativo de entrada. Para especificar uma chave de acesso (mnemônica não emlinada) para a **Legenda,** inclua um caractere & (entese) antes desse caractere.

Se você definir comandos para uma coleção [**De**](/windows/desktop/lwef/the-commands-collection-object) comandos que tem uma [**Legenda**](caption-property.md), normalmente também definirá uma **Legenda** para sua coleção **de Comandos** associada.

 

 
