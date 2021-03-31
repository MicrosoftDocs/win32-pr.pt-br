---
title: Propriedade VoiceCaption (objeto Commands)
description: Propriedade VoiceCaption
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644144"
---
# <a name="voicecaption-property-commands-object"></a>Propriedade VoiceCaption (objeto Commands)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o texto exibido para o objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) na janela de comandos de voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Caracteres Agent. ***("**_characterid_*_"). String Commands. VoiceCaption_ *  \[  =  \]



| Parte     | Descrição                                               |
|----------|-----------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada como o texto exibido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você definir a propriedade de [**voz**](voice-property.md) da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , normalmente também definirá sua propriedade **VoiceCaption** . A configuração texto de **VoiceCaption** aparece na janela comandos de voz quando o aplicativo cliente é de entrada-ativo e o caractere é visível. Se essa propriedade não for definida, a configuração da propriedade [**Caption**](caption-property.md) da coleção de **comandos** determinará o texto exibido. Quando a propriedade **VoiceCaption** ou **Caption** for definida, os comandos na coleção aparecerão na janela de comandos de voz em "(comando indefinido)" quando o aplicativo cliente se tornar entrada-ativo.

A configuração **VoiceCaption** também determina o texto exibido na dica de escuta para indicar os comandos para os quais o caractere escuta.

## <a name="see-also"></a>Consulte Também

[Propriedade Caption](caption-property.md)


 

 
