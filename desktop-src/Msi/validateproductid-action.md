---
description: A ação ValidateProductID define a propriedade ProductID para o identificador completo do produto.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Ação ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752022"
---
# <a name="validateproductid-action"></a>Ação ValidateProductID

A ação ValidateProductID define a propriedade [**ProductID**](productid.md) para o identificador completo do produto.

## <a name="sequence-restrictions"></a>Restrições de sequência

Essa ação deve ser sequenciada antes do assistente de interface do usuário na [tabela InstallUISequence](installuisequence-table.md) e antes da [ação RegisterUser](registeruser-action.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

O instalador verifica se um produto foi validado com êxito verificando a propriedade [**ProductID**](productid.md) . O instalador define a propriedade **ProductID** para o identificador completo do produto após uma validação bem-sucedida. A ação ValidateProductID não fará nada se a propriedade **ProductID** já tiver sido definida por uma validação bem-sucedida ou por outro método.

A ação ValidateProductID sempre retorna um sucesso, independentemente de o identificador do produto ser válido, para que o identificador do produto possa ser inserido na linha de comando na primeira vez em que o produto for executado.

O identificador do produto pode ser validado sem que o usuário insira novamente essas informações definindo a propriedade [**PIDKEY**](pidkey.md) na linha de comando ou usando uma transformação. A exibição da caixa de diálogo solicitando que o usuário insira o identificador do produto pode então se tornar condicional após a presença da propriedade [**ProductID**](productid.md) , que é definida quando a propriedade **PIDKEY** é validada.

 

 



