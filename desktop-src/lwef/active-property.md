---
title: Propriedade Ativa
description: Propriedade Ativa
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac75a83724c793f2a7aba01718d57e47b25a0dd6b467ca7797ad6f0e4ced018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753165"
---
# <a name="active-property"></a>Propriedade Ativa

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna se o aplicativo é o cliente ativo do caractere e se o caractere é mais alto.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters***("**_CharacterID_*_"). Estado_ *  \[  =  *Ativo*\]



| Parte    | Descrição                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Uma expressão de inteiro que especifica o estado do aplicativo cliente. 0 Não é o cliente ativo.<br/> 1 O cliente ativo. <br/> 2 O cliente ativo de entrada. (O caractere mais alto.)<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do [](click-event.md) caractere recebe entrada do mouse (por exemplo, eventos Click ou [DragStart](dragstart-event.md) do controle do Microsoft Agent). Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere mais alto (também conhecido como cliente ativo de entrada) recebe eventos command.

Você pode usar o método [**Activate**](activate-method.md)para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente ativo de entrada (que também torna o caractere mais alto).

## <a name="see-also"></a>Consulte Também

[Método Activate** **](activate-method.md)


 

 





