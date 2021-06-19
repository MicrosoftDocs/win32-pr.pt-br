---
title: Propriedade Enabled (objeto Command)
description: Saiba mais sobre a propriedade de objeto Comando Habilitado. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407329"
---
# <a name="enabled-property-command-object"></a>Propriedade Enabled (objeto Command)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define se **o Comando** está habilitado no menu pop-up do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_"). Booliana_ *  \[  =  *habilitada*\]



| Parte      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se **o Comando** está habilitado.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdadeiro**</dt> <dd> O **Comando** está habilitado.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Falso**</dt> <dd> O **Comando** está desabilitado.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a [**propriedade Habilitado**](enabled-property.md) estiver definida [](/windows/desktop/lwef/the-command-object) como **True**, a legenda dos objetos Command aparecerá como texto normal no menu pop-up do caractere quando o aplicativo cliente estiver ativo de entrada. Se a **propriedade Enabled** for **False**, a legenda aparecerá como texto indisponível (desabilitado). Um Comando **desabilitado** também não está acessível para entrada de voz.

 

