---
title: Propriedade Caption (objeto de coleção de comandos)
description: Propriedade Caption
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085067"
---
# <a name="caption-property-commands-collection-object"></a>Propriedade Caption (objeto de coleção de comandos)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Determina o texto exibido para um objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_")._ * Cadeia de caracteres [Commands. Caption](caption-property.md) \[  =  \]



| Parte     | Descrição                                                              |
|----------|--------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada como o texto exibido como a legenda. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Definir a propriedade [**Caption**](caption-property.md) para sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) define como ela será exibida no menu pop-up do caractere quando sua propriedade [**Visible**](visible-property.md) é definida como true e seu aplicativo não é o cliente de entrada-ativo. Para especificar uma tecla de acesso (mnemônico não embutido) para sua **legenda**, inclua um caractere de e comercial (&) antes desse caractere.

Se você definir comandos para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) que tenha uma [**legenda**](caption-property.md), normalmente também definirá uma **legenda** para sua coleção de **comandos** associada.

 

 
