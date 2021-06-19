---
title: Propriedade VoiceCaption (objeto Commands)
description: Saiba mais sobre a Propriedade VoiceCaption do objeto Commands, que retorna ou define o texto exibido para o objeto Comandos na janela Comandos de Voz.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396121"
---
# <a name="voicecaption-property-commands-object"></a>Propriedade VoiceCaption (objeto Commands)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define o texto exibido para o objeto [**Comandos**](/windows/desktop/lwef/the-commands-collection-object) na Janela Comandos de Voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Cadeia de caracteres Commands.VoiceCaption_ *  \[  =  \]



| Parte     | Descrição                                               |
|----------|-----------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada para o texto exibido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você definir a [**propriedade Voz**](voice-property.md) da coleção [**Comandos,**](/windows/desktop/lwef/the-commands-collection-object) normalmente também definirá sua **propriedade VoiceCaption.** A **configuração de texto VoiceCaption** aparece na Janela Comandos de Voz quando o aplicativo cliente está ativo de entrada e o caractere está visível. Se essa propriedade não estiver definida, a configuração da propriedade [**Legenda**](caption-property.md) da coleção **Comandos** determinará o texto exibido. Quando a propriedade **VoiceCaption** ou **Caption** não estiver definida, os comandos na coleção aparecerão na Janela comandos de voz em "(comando indefinido)" quando o aplicativo cliente se tornar input-active.

A **configuração VoiceCaption** também determina o texto exibido na Dica de Escuta para indicar os comandos para os quais o caractere escuta.

## <a name="see-also"></a>Consulte Também

[Propriedade Caption](caption-property.md)


 

 
