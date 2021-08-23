---
title: Propriedade Name (objeto Characters)
description: Saiba mais sobre a propriedade Name do objeto Characters. O Microsoft Agent foi preterido a partir Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08509d5d2a349c56548259db4846203da6f632ff76c86309db87e6aa90583a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608646"
---
# <a name="name-property-characters-object"></a>Propriedade Name (objeto Characters)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define uma cadeia de caracteres que especifica o nome padrão do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Cadeia de_ *  \[  =  *caracteres de nome*\]



| Parte     | Descrição                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Um valor de cadeia de caracteres correspondente ao nome do caractere (na configuração de idioma atual). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O Nome de um **caractere** pode depender da configuração [**LanguageID do**](languageid-property.md) caractere. O nome de um caractere em um idioma pode ser diferente ou usar caracteres diferentes de outro. O Nome padrão do caractere **para** um idioma específico é definido quando o caractere é compilado com o Editor de Caracteres do Microsoft Agent.

Evite renomear um caractere, especialmente ao usá-lo em um cenário em que outros aplicativos cliente podem usar o mesmo caractere. Além disso, o Agent usa o Nome **do** caractere para criar comandos automaticamente para ocultar e mostrar o caractere.

 

 




