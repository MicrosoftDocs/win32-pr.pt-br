---
description: O instalador armazena todas as informações sobre a interface do usuário nas tabelas do banco de dados de instalação.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Visualizando a interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169845"
---
# <a name="previewing-the-user-interface"></a>Visualizando a interface do usuário

O instalador armazena todas as informações sobre a [interface do usuário](user-interface.md) nas tabelas do banco de dados de instalação. Para facilitar o design da interface do usuário, o instalador também fornece um modo de visualização para exibir essas informações. O procedimento a seguir descreve como habilitar o modo de visualização da interface do usuário e exibir a aparência atual de caixas de diálogo e de murals.

**Para exibir a interface do usuário no modo de visualização**

1.  Habilite o modo de visualização chamando a função [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .
2.  Exiba as caixas de diálogo específicas chamando a função [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .
3.  Exiba os murals específicos chamando a função [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .

 

 



