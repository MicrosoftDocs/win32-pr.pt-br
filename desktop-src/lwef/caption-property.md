---
title: Propriedade Caption (objeto Command)
description: Propriedade Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105771669"
---
# <a name="caption-property-command-object"></a>Propriedade Caption (objeto Command)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Determina o texto exibido para um [**comando**](/windows/desktop/lwef/the-command-object) no menu pop-up do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_"). Comandos ("_*_Name_*_")._ *  \[  =  *Cadeia de caracteres* de legenda\]



| Parte     | Descrição                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada como o texto exibido como a legenda do **comando**. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Para especificar uma tecla de acesso (mnemônico não embutido) para sua **legenda**, inclua um caractere de e comercial (&) antes desse caractere.

Se você não definir um **VoiceCaption** para o comando, sua configuração de **legenda** será usada.

 

 
