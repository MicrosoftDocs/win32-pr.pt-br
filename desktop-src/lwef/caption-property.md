---
title: Propriedade Caption (objeto Command)
description: Saiba mais sobre a propriedade Caption do objeto Command. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262548"
---
# <a name="caption-property-command-object"></a>Propriedade Caption (objeto Command)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Determina o texto exibido para um [**Comando**](/windows/desktop/lwef/the-command-object) no menu pop-up do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_"). Cadeia de_ *  \[  =  *caracteres* de legenda\]



| Parte     | Descrição                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada para o texto exibido como a legenda do **Comando**. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Para especificar uma chave de acesso (mnemônico não emlindado) para a **Legenda**, inclua um caractere & (entese) antes desse caractere.

Se você não definir uma **VoiceCaption para** seu comando, a **configuração Legenda** será usada.

 

 
