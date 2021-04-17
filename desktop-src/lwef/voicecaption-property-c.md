---
title: Propriedade VoiceCaption (objeto Command)
description: Propriedade VoiceCaption
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105812371"
---
# <a name="voicecaption-property-command-object"></a>Propriedade VoiceCaption (objeto Command)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Define ou retorna o texto exibido para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) na janela comandos de voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Caracteres Agent. ***("**_characterid_*_"). Comandos ("_*_Name_*_")._ *  \[  =  *Cadeia de caracteres* VoiceCaption\]



| Parte     | Descrição                                               |
|----------|-----------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada como o texto exibido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você definir um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](https://www.bing.com/search?q=**Commands**) e definir sua propriedade de [**voz**](voice-property.md) , normalmente também definirá sua propriedade [**VoiceCaption**](voicecaption-property.md) . Esse texto será exibido na janela de comandos de voz quando o aplicativo cliente for de entrada-ativo e o caractere estiver visível. Se essa propriedade não for definida, a configuração da propriedade [**Caption**](caption-property.md) determinará o texto exibido. Quando nem a propriedade **VoiceCaption** nem **Caption** é definida, o comando não aparece na janela de comandos de voz.

### <a name="see-also"></a>Consulte Também

[**Propriedade Caption**](caption-property.md)


 

 
