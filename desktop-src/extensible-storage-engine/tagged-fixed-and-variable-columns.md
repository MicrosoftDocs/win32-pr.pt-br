---
description: 'Saiba mais sobre: colunas marcadas, fixas e variáveis'
title: Colunas marcadas, fixas e variáveis
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461097"
---
# <a name="tagged-fixed-and-variable-columns"></a>Colunas marcadas, fixas e variáveis


_**Aplica-se a:** Windows | Windows Server_

## <a name="tagged-fixed-and-variable-columns"></a>Colunas marcadas, fixas e variáveis

Colunas marcadas, fixas e de comprimento variável são os tipos de coluna principais com suporte do ESE. As colunas marcadas não estão presentes em um registro, a menos que os dados sejam armazenados na coluna e possam ser fixos ou ter comprimento variável. As colunas marcadas também podem conter mais de um valor em um único registro. As colunas fixas assumem a mesma quantidade de espaço em cada linha e exigem 1 bit para representar o valor nulo. Colunas de comprimento variável exigem 2 bytes para representar o tamanho e o valor nulo e ocupam uma quantidade variável de espaço em cada registro. Para obter mais informações sobre as colunas marcadas e fixas, consulte a Jet_bitColumnTagged e Jet_bitColumnFixed opção no membro **grbit** da estrutura [JET_COLUMNDEF](./jet-columndef-structure.md) usada na chamada para [JetAddColumn](./jetaddcolumn-function.md).

Colunas de comprimento variável são determinadas pelo tipo de coluna que é definido no parâmetro *coltyp* na chamada de [JetAddColumn](./jetaddcolumn-function.md). Os tipos de coluna a seguir podem ser fixos ou ter comprimento variável, dependendo se a opção de Jet_bitColumnFixed está definida:

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

Em geral, os dados no registro são armazenados com o intervalo fixo primeiro, o intervalo de variáveis Next e o intervalo marcado armazenado por último. O diagrama a seguir mostra como os registros são armazenados na tabela. Conforme mostrado no diagrama, o intervalo marcado pode conter colunas com vários valores.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
