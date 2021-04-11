---
title: Propriedade ativa
description: Propriedade ativa
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159807"
---
# <a name="active-property"></a>Propriedade ativa

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna se seu aplicativo é o cliente ativo do caractere e se o caractere está no nível mais alto.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do. ***Caracteres * * * * ("*** characterid * * *").* *  \[  =  *Estado* ativo\]



| Parte    | Descrição                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Uma expressão de inteiro que especifica o estado do seu aplicativo cliente. 0 não é o cliente ativo.<br/> 1 o cliente ativo. <br/> 2 o cliente de entrada-ativo. (O caractere superior).<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe a entrada do mouse (por exemplo, os eventos [**Click**](click-event.md) ou [DragStart](dragstart-event.md) do controle do Microsoft Agent). Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere superior (também conhecido como o cliente de entrada-ativo) recebe eventos de comando.

Você pode usar o método [**Activate**](activate-method.md)para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente de entrada ativo (o que também torna o caractere mais alto).

## <a name="see-also"></a>Consulte Também

[Ativar * * método * *](activate-method.md)


 

 





