---
description: Uma sequência de caixa de diálogo FirstRun coleta informações de nome de usuário, nome da empresa e ID do produto. O instalador verifica a ID do produto durante essa caixa de diálogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Caixa de diálogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de44417014aefb84d2d381166d5a2fceb7f956c4212e9dba31556053c583fef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828886"
---
# <a name="firstrun-dialog"></a>Caixa de diálogo FirstRun

Uma sequência de caixa de diálogo FirstRun coleta informações de nome de usuário, nome da empresa e ID do produto. O instalador verifica a ID do produto durante essa caixa de diálogo.

Uma sequência de caixa de diálogo FirstRun geralmente não faz parte da sequência de ação e é chamada pela função [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) na primeira sequência do produto.

Um autor de um pacote do instalador pode usar a sequência de diálogo de modelo ou criar uma sequência diferente. No entanto, a sequência de diálogo precisa fazer o usuário definir as seguintes propriedades:

-   [**Propriedade USERNAME**](username.md)
-   [**Propriedade COMPANYNAME**](companyname.md)
-   [**Propriedade PIDKEY**](pidkey.md)

A ID do produto será validada durante a caixa de diálogo usando [a ação ValidateProductID](validateproductid-action.md) ou [ValidateProductID ControlEvent](validateproductid-controlevent.md).

Se a ID do produto for definida como uma propriedade na linha de comando ou por uma transformação, a necessidade de fazer com que o usuário reinsera a ID do produto durante a caixa de diálogo de primeira sequência poderá ser contornada controlando a exibição usando a [**propriedade ProductID.**](productid.md) Após a validação bem-sucedida da ID do produto, a **propriedade ProductID** é definida como a ID do produto completa e válida.

 

 



