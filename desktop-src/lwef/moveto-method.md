---
title: Método MoveTo
description: Método MoveTo
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a245d389bc23d79d9f6cc105fec28ed14f5d511123c1dd113115ff69fc95c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609076"
---
# <a name="moveto-method"></a>Método MoveTo

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Move o caractere especificado para o local especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Velocidade de MoveTo_ *  *x,y* \[ \]



| Parte    | Descrição                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y*   | Obrigatórios. Um valor inteiro que indica a borda esquerda (*x*) e a borda superior (*y*) do quadro de animação. Expresse essas coordenadas em pixels.                                                   |
| *Velocidade* | Opcional. Um valor inteiro longo que especifica em milissegundos a rapidez com que o quadro do caractere se move. O valor padrão é 1000. Especificar zero (0) move o quadro sem a reprodução de uma animação. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O servidor reproduz automaticamente a animação apropriada atribuída aos **estados Em** movimento. O local de um caractere é baseado no canto superior esquerdo de seu quadro.

Se você declarar uma variável de objeto e defini-la para esse método, ela retornará um [**objeto Request.**](/windows/desktop/lwef/the-request-object) Além disso, se a animação associada não tiver sido carregada  no computador local, o servidor define a propriedade [**Status**](status-property.md) do objeto Request como "failed" com um número de erro apropriado. Portanto, se você estiver usando o protocolo HTTP para acessar dados  de caractere ou animação, use o método [**Get**](get-method.md) para carregar as animações de estado De movimentação antes de chamar o **método MoveTo.**

Mesmo que a animação não seja carregada, o servidor ainda move o quadro.

> [!Note]  
> Se você chamar **MoveTo** com um valor diferente de zero antes que o caractere seja mostrado, ele retornará um status de falha se você tiver atribuído a ele um objeto [**Request,**](/windows/desktop/lwef/the-request-object) porque o valor diferente de zero indica que você está tentando reproduzir uma animação quando o caractere não está visível.

 

> [!Note]  
> O *efeito* real do parâmetro Speed pode variar com base na velocidade do processador do computador e na prioridade de outras tarefas em execução no sistema.

 

 

 