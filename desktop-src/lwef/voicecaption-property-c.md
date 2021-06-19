---
title: Propriedade VoiceCaption (objeto Command)
description: Saiba mais sobre a Propriedade VoiceCaption do objeto Command, que define ou retorna o texto exibido para o objeto Command na janela Comandos de Voz.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396161"
---
# <a name="voicecaption-property-command-object"></a>Propriedade VoiceCaption (objeto Command)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Define ou retorna o texto exibido para o [**objeto Command**](/windows/desktop/lwef/the-command-object) na Janela Comandos de Voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands("_*_Name_*_"). Cadeia de caracteres_ *  \[  =  *VoiceCaption*\]



| Parte     | Descrição                                               |
|----------|-----------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada para o texto exibido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você definir um [**objeto Command**](/windows/desktop/lwef/the-command-object) em uma coleção [**Commands**](https://www.bing.com/search?q=**Commands**) e definir sua propriedade [**Voice,**](voice-property.md) normalmente também definirá sua [**propriedade VoiceCaption.**](voicecaption-property.md) Esse texto será exibido na Janela Comandos de Voz quando o aplicativo cliente estiver ativo de entrada e o caractere estiver visível. Se essa propriedade não estiver definida, a configuração da propriedade [**Legenda**](caption-property.md) determinará o texto exibido. Quando a **propriedade VoiceCaption** nem **Caption** não é definida, o comando não aparece na janela Comandos de Voz.

### <a name="see-also"></a>Consulte Também

[**Propriedade Caption**](caption-property.md)


 

 
