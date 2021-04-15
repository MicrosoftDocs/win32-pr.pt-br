---
description: Se esse bit for definido, a caixa de diálogo será modal, outras caixas de diálogo do mesmo aplicativo não poderão ser colocadas sobre ele, e o diálogo manterá o controle enquanto estiver em execução.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit de estilo de caixa de diálogo modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506093"
---
# <a name="modal-dialog-style-bit"></a>Bit de estilo de caixa de diálogo modal

Se esse bit for definido, a caixa de diálogo será modal, outras caixas de diálogo do mesmo aplicativo não poderão ser colocadas sobre ele, e o diálogo manterá o controle enquanto estiver em execução. Se esse bit não for definido, a caixa de diálogo será sem janela restrita, outras caixas de diálogo do mesmo aplicativo poderão ser movidas sobre ele. Depois que uma caixa de diálogo sem janela restrita é criada e exibida, a interface do usuário retorna o controle ao instalador. Em seguida, o instalador chama a interface do usuário periodicamente para atualizar a caixa de diálogo e dar a ela a oportunidade de processar as mensagens. Assim que isso for feito, o controle será retornado para o instalador.

> [!Note]  
> Não deve haver caixas de diálogo sem janela restrita em uma sequência de assistente, pois isso retornará o controle ao instalador, encerrando a sequência do assistente prematuramente.

 

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



