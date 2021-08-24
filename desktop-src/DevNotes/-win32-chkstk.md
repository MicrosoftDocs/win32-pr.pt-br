---
description: Chamado pelo compilador quando você tem mais de uma página de variáveis locais em sua função.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk rotina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b129b73801c6c18b63b10ac61898ee13a9c5d4f1f0422678bbfe5af82d5b44f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538826"
---
# <a name="_chkstk-routine"></a>\_Rotina chkstk

Chamado pelo compilador quando você tem mais de uma página de variáveis locais em sua função.

## <a name="remarks"></a>Comentários

\_Chkstk Routine é uma rotina auxiliar para o compilador C. Para compiladores x86, a rotina chkstk é chamada quando as variáveis locais excedem \_ 4K bytes; para compiladores x64, é de 8K.

 

 



