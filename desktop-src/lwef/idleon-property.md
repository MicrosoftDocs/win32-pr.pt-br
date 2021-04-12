---
title: Propriedade idleize
description: Propriedade idleize
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291738"
---
# <a name="idleon-property"></a>Propriedade idleize

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define um valor booliano que determina se o servidor gerencia as animações de estado **deixar** do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *").* *  \[  =  *Booliano* de ociosidade\]

</dd> </dl> 

| Parte      | Descrição                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o servidor gerencia o modo ocioso. **True** (padrão) a manipulação de servidor do estado ocioso está habilitada. <br/> **Falso** A manipulação de servidor do estado ocioso está desabilitada. <br/> |



 

## <a name="remarks"></a>Comentários

O servidor define automaticamente um tempo limite após a última animação executada para um caractere. Quando o intervalo desse temporizador for concluído, o servidor começará o estado **deixar** de um caractere, jogando suas animações **deixar** associadas em intervalos regulares. Se você quiser desabilitar o servidor de reproduzir automaticamente as animações de estado **deixar** , defina a propriedade como **false** e reproduza uma animação ou chame o método [**Stop**](stop-method.md) . A definição desse valor não afeta o estado de animação atual do caractere.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

 

 





