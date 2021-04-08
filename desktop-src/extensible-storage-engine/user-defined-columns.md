---
description: 'Saiba mais sobre: colunas definidas pelo usuário'
title: Colunas definidas pelo usuário
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010745"
---
# <a name="user-defined-columns"></a>Colunas definidas pelo usuário


_**Aplica-se a:** Windows | Windows Server_

## <a name="user-defined-columns"></a>Colunas definidas pelo usuário

As colunas definidas pelo usuário são colunas cujos valores padrão são fornecidos por uma função de retorno de chamada. Essas colunas são sempre marcadas e definidas com o valor calculado pela função de retorno de chamada. Esse valor deve ser estável para cada linha na tabela. A função de retorno de chamada só é usada quando o aplicativo ou o mecanismo de banco de dados precisa ler o valor da coluna para uma determinada linha. O aplicativo tem a opção de substituir o valor padrão e definir um valor específico na coluna. Quando o valor padrão é substituído nas colunas, ele usa o espaço na linha; caso contrário, as colunas padrão definidas pelo usuário não usam espaço no registro.

A opção padrões definidos pelo usuário é definida no membro **grbit** da estrutura [JET_COLUMNDEF](./jet-columndef-structure.md) na chamada de [JetAddColumn](./jetaddcolumn-function.md). O parâmetro *pvDefault* da função [JetAddColumn](./jetaddcolumn-function.md) aponta para uma estrutura de [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , que contém o nome da função de retorno de chamada no membro **szCallback** , e os dados que são passados para o retorno de chamada no membro **pbUserData** .
