---
description: O instalador armazena todas as informações sobre a interface do usuário nas tabelas do banco de dados de instalação.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Visualizando o Interface do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738387ac834d4e9c26f4a413755dce0c5abdc5e421cc4ef88b1f9b41054f201d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082656"
---
# <a name="previewing-the-user-interface"></a>Visualizando o Interface do Usuário

O instalador armazena todas as informações sobre a [interface do usuário](user-interface.md) nas tabelas do banco de dados de instalação. Para facilitar o design da interface do usuário, o instalador também fornece um modo de visualização para exibir essas informações. O procedimento a seguir descreve como habilitar o modo de visualização da interface do usuário e exibir a aparência atual de caixas de diálogo e painéis.

**Para exibir a interface do usuário no modo de visualização**

1.  Habilita o modo de visualização chamando a [**função MsiEnableUIPreview.**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
2.  Exibe as caixas de diálogo específicas chamando a [**função MsiPreviewDialog.**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
3.  Exibir determinados painéis chamando a [**função MsiPreviewBillboard.**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)

 

 



