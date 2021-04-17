---
description: Se esse bit for definido, a caixa de diálogo será um diálogo de erro.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit de estilo de caixa de diálogo de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748594"
---
# <a name="error-dialog-style-bit"></a>Bit de estilo de caixa de diálogo de erro

Se esse bit for definido, a caixa de diálogo será um diálogo de erro.

Pode haver mais de uma caixa de diálogo com este estilo. A propriedade **ErrorDialog** determina qual caixa de diálogo é usada como uma caixa de diálogo de erro. A caixa de diálogo selecionada pode ser apenas uma das que têm esse conjunto de bits de estilo. A caixa de diálogo de erro deve ter um controle de texto estático chamado ErrorText. Esse controle recebe o texto da mensagem de erro. A caixa de diálogo também deve ter os sete botões de push correspondentes aos possíveis valores de retorno. A mensagem de erro determina quais desses botões são realmente exibidos. Os botões exibidos são reorganizados para que sejam distribuídos uniformemente na caixa de diálogo. Essa reorganização altera a coordenada X dos botões, mas não as outras três coordenadas. Portanto, é aconselhável que nenhum outro controle seja criado na mesma região horizontal da caixa de diálogo que os botões. Se a mensagem de erro não especificar nenhum botão, o botão **OK** será exibido. O botão **padrão** , o primeiro controle ativo e os valores de botão de **cancelamento** são ignorados para uma caixa de diálogo de erro. O botão **padrão** definido na mensagem de erro será atribuído a todos os três valores. O efeito de enviar esses botões deve ser definido na [tabela ControlEvent,](controlevent-table.md) , assim como para todos os outros botões. O título da caixa de diálogo é criado de forma semelhante a outras caixas de diálogo. Ele poderá ser substituído pela mensagem de erro se especificar um texto de cabeçalho após a lista de botões.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                       |
|---------|-------------|--------------------------------|
| 65536   | 0x00010000  | **msidbDialogAttributesError** |



 

 

 



