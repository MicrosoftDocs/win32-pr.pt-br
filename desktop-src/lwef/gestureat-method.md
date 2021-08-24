---
title: Método GestureAt
description: Método GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c18c2a3913e8c9e805725f184bd5e969de6272ed05c562799805bd8c74256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725716"
---
# <a name="gestureat-method"></a>Método GestureAt

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Reproduz a animação gesturing para o caractere especificado no local especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_"). GestureAt_ *  *x, y*



| Parte  | Descrição                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y* | Obrigatórios. Um valor inteiro que indica a coordenada de tela horizontal (*x*) e a coordenada de tela vertical (*y*) para a qual o caractere será gestodo. Essas coordenadas devem ser especificadas em pixels. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O servidor desempenha automaticamente a animação apropriada para gestor em direção ao local especificado. As coordenadas são sempre relativas à origem da tela (superior esquerda).

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Além disso, se a animação associada não tiver sido carregada no computador local, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado. Portanto, se você estiver usando o protocolo HTTP para acessar dados de animação de caracteres, use o método [**Get**](get-method.md) para carregar as animações de estado **gesturing** antes de chamar o método **GestureAt** .

 

 