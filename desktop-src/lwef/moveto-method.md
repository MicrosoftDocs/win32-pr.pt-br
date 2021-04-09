---
title: Método MoveTo
description: Método MoveTo
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007549"
---
# <a name="moveto-method"></a>Método MoveTo

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Move o caractere especificado para o local especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *").* *  *Velocidade de x, y* \[ \]



| Parte    | Descrição                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y*   | Obrigatórios. Um valor inteiro que indica a borda esquerda (*x*) e a borda superior (*y*) do quadro de animação. Expresse essas coordenadas em pixels.                                                   |
| *Velocidade* | Opcional. Um valor inteiro longo que especifica em milissegundos a velocidade com que o quadro do caractere se move. O valor padrão é 1000. A especificação de zero (0) move o quadro sem reproduzir uma animação. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O servidor desempenha automaticamente a animação apropriada atribuída aos Estados de **movimentação** . O local de um caractere é baseado no canto superior esquerdo de seu quadro.

Se você declarar uma variável de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Além disso, se a animação associada não tiver sido carregada no computador local, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado. Portanto, se você estiver usando o protocolo HTTP para acessar dados de caracteres ou de animação, use o método [**Get**](get-method.md) para carregar as animações de estado de **movimentação** antes de chamar o método **MoveTo** .

Mesmo que a animação não seja carregada, o servidor ainda moverá o quadro.

> [!Note]  
> Se você chamar **MoveTo** com um valor diferente de zero antes de o caractere ser mostrado, ele retornará um status de falha se você atribuiu a ele um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) , porque o valor diferente de zero indica que você está tentando reproduzir uma animação quando o caractere não está visível.

 

> [!Note]  
> O efeito real do parâmetro de *velocidade* pode variar com base na velocidade do processador do computador e na prioridade de outras tarefas em execução no sistema.

 

 

 