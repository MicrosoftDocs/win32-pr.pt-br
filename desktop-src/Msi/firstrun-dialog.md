---
description: Uma sequência da caixa de diálogo FirstRun coleta o nome do usuário, o nome da empresa e as informações de ID do produto. O instalador verifica a ID do produto durante esta caixa de diálogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Caixa de diálogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165001"
---
# <a name="firstrun-dialog"></a>Caixa de diálogo FirstRun

Uma sequência da caixa de diálogo FirstRun coleta o nome do usuário, o nome da empresa e as informações de ID do produto. O instalador verifica a ID do produto durante esta caixa de diálogo.

Uma sequência de caixa de diálogo FirstRun geralmente não faz parte da sequência de ação e é chamada pela função [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) na primeira execução do produto.

Um autor de um pacote do instalador pode usar a sequência de diálogo de modelo ou criar uma sequência diferente. No entanto, a sequência de diálogo precisa ter o usuário definido as seguintes propriedades:

-   Propriedade [**username**](username.md)
-   Propriedade [**CompanyName**](companyname.md)
-   Propriedade [**PIDKEY**](pidkey.md)

A ID do produto será validada durante a caixa de diálogo usando a [ação ValidateProductID](validateproductid-action.md) ou [ValidateProductID ControlEvent,](validateproductid-controlevent.md).

Se a ID do produto for definida como uma propriedade na linha de comando ou por uma transformação, a necessidade de fazer com que o usuário insira novamente a ID do produto durante a caixa de diálogo de primeira execução poderá ser contornada controlando a exibição usando a propriedade [**ProductID**](productid.md) . Após a validação bem-sucedida da ID do produto, a propriedade **ProductID** é definida como a ID de produto completa válida.

 

 



