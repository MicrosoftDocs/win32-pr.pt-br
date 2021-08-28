---
title: Propriedade IdleOn
description: Propriedade IdleOn
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e08ada4d48197e3090b5fc821b0c5b9f532f47074985218019bb14be8881e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749503"
---
# <a name="idleon-property"></a>Propriedade IdleOn

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define um valor booliana que determina se o servidor gerencia as animações de estado **de Idling** do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Booliana IdleOn_ *  \[  =  \]

</dd> </dl> 

| Parte      | Descrição                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o servidor gerencia o modo ocioso. **A** manipulação de servidor True (Padrão) do estado ocioso está habilitada. <br/> **False** A manipulação do servidor do estado ocioso está desabilitada. <br/> |



 

## <a name="remarks"></a>Comentários

O servidor define automaticamente um tempo-out após a última animação tocada para um caractere. Quando o intervalo desse temporizador for concluído, o servidor começará o estado de **Idling** de um caractere, tocando suas animações de **Idling** associadas em intervalos regulares. Se você quiser desabilitar o servidor de reproduzir automaticamente as animações de estado de **Idling,** de definir a propriedade como **False** e reproduzir uma animação ou chamar o [**método Stop.**](stop-method.md) Definir esse valor não afeta o estado de animação atual do caractere.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

 

 





