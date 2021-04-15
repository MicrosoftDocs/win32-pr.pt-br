---
title: Sinalizadores de inicialização de caixa de diálogo comum
description: Os sinalizadores são usados para modificar o comportamento e a aparência de uma caixa de diálogo comum.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Biblioteca de caixa de diálogo comum, inicializando
- caixas de diálogo comuns, inicializando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/19/2020
ms.locfileid: "104454484"
---
# <a name="common-dialog-box-initialization-flags"></a>Sinalizadores de inicialização de caixa de diálogo comum

Os sinalizadores são usados para modificar o comportamento e a aparência de uma caixa de diálogo comum. Os sinalizadores de inicialização são os valores que você define no membro **flags** da estrutura que é usada para criar a caixa de diálogo. Você usa os sinalizadores para especificar quais controles em uma caixa de diálogo recebem valores iniciais, para desabilitar os controles selecionados e para modificar o intervalo de valores que o usuário pode definir com os controles. Você também usa os sinalizadores para habilitar os procedimentos de conexão e modelos personalizados para as caixas de diálogo.

Por exemplo, você pode definir o valor de **\_ efeitos do CF** no membro **flags** da estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para direcionar a caixa de diálogo **fonte** para exibir os controles de efeitos. Esses controles permitem que o usuário escolha uma cor de fonte, bem como efeitos de tachado e sublinhado.

Os valores do sinalizador de inicialização são exclusivos de cada caixa de diálogo comum e são descritos detalhadamente pelos membros dos **sinalizadores** das seguintes estruturas que correspondem a eles:

-   [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [**DA OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




