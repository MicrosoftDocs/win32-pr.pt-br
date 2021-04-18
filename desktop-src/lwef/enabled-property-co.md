---
title: Propriedade Enabled (objeto Command)
description: Propriedade Enabled
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105790492"
---
# <a name="enabled-property-command-object"></a>Propriedade Enabled (objeto Command)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define se o **comando** está habilitado no menu pop-up do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_"). Comandos ("_*_Name_*_")._ *  \[  =  *Booliano* habilitado\]



| Parte      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o **comando** está habilitado.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt> <dd> O **comando** está habilitado.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**For**</dt> <dd> O **comando** está desabilitado.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a propriedade [**Enabled**](enabled-property.md) for definida como **true**, a legenda dos objetos de [**comando**](/windows/desktop/lwef/the-command-object) aparecerá como texto normal no menu pop-up do caractere quando o aplicativo cliente for Input-active. Se a propriedade **Enabled** for **false**, a legenda aparecerá como texto indisponível (desabilitado). Um **comando** desabilitado também não está acessível para entrada de voz.

 

