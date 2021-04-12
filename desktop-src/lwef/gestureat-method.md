---
title: Método GestureAt
description: Método GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453986"
---
# <a name="gestureat-method"></a>Método GestureAt

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Reproduz a animação gesturing para o caractere especificado no local especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). GestureAt* *  *x, y*



| Parte  | Descrição                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y* | Obrigatórios. Um valor inteiro que indica a coordenada de tela horizontal (*x*) e a coordenada de tela vertical (*y*) para a qual o caractere será gestodo. Essas coordenadas devem ser especificadas em pixels. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O servidor desempenha automaticamente a animação apropriada para gestor em direção ao local especificado. As coordenadas são sempre relativas à origem da tela (superior esquerda).

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Além disso, se a animação associada não tiver sido carregada no computador local, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado. Portanto, se você estiver usando o protocolo HTTP para acessar dados de animação de caracteres, use o método [**Get**](get-method.md) para carregar as animações de estado **gesturing** antes de chamar o método **GestureAt** .

 

 