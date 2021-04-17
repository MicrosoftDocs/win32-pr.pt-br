---
title: Propriedade Name (objeto characters)
description: Propriedade Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454520"
---
# <a name="name-property-characters-object"></a>Propriedade Name (objeto characters)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define uma cadeia de caracteres que especifica o nome padrão do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_")._ *  \[  =  *Cadeia de caracteres* de nome\]



| Parte     | Descrição                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Um valor de cadeia de caracteres correspondente ao nome do caractere (na configuração de idioma atual). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O **nome** de um caractere pode depender da configuração [**LanguageID**](languageid-property.md) do caractere. O nome de um caractere em um idioma pode ser diferente ou usar caracteres diferentes do que em outro. O **nome** padrão do caractere para um idioma específico é definido quando o caractere é compilado com o editor de caracteres do Microsoft Agent.

Evite renomear um caractere, especialmente ao usá-lo em um cenário em que outros aplicativos cliente possam usar o mesmo caractere. Além disso, o Agent usa o **nome** do caractere para criar automaticamente comandos para ocultar e mostrar o caractere.

 

 




