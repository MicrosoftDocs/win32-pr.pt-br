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
# <a name="previewing-the-user-interface"></a><span data-ttu-id="aabbf-103">Visualizando a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="aabbf-103">Previewing the User Interface</span></span>

<span data-ttu-id="aabbf-104">O instalador armazena todas as informações sobre a [interface do usuário](user-interface.md) nas tabelas do banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="aabbf-104">The installer stores all information about the [user interface](user-interface.md) in the tables of the installation database.</span></span> <span data-ttu-id="aabbf-105">Para facilitar o design da interface do usuário, o instalador também fornece um modo de visualização para exibir essas informações.</span><span class="sxs-lookup"><span data-stu-id="aabbf-105">To facilitate the design of the UI the installer also provides a preview mode for viewing this information.</span></span> <span data-ttu-id="aabbf-106">O procedimento a seguir descreve como habilitar o modo de visualização da interface do usuário e exibir a aparência atual de caixas de diálogo e de murals.</span><span class="sxs-lookup"><span data-stu-id="aabbf-106">The following procedure describes how to enable the UI preview mode and display the current appearance of dialog boxes and billboards.</span></span>

<span data-ttu-id="aabbf-107">**Para exibir a interface do usuário no modo de visualização**</span><span class="sxs-lookup"><span data-stu-id="aabbf-107">**To view the user interface in the preview mode**</span></span>

1.  <span data-ttu-id="aabbf-108">Habilite o modo de visualização chamando a função [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .</span><span class="sxs-lookup"><span data-stu-id="aabbf-108">Enable the preview mode by calling the [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) function.</span></span>
2.  <span data-ttu-id="aabbf-109">Exiba as caixas de diálogo específicas chamando a função [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .</span><span class="sxs-lookup"><span data-stu-id="aabbf-109">Display the particular dialog boxes by calling the [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) function.</span></span>
3.  <span data-ttu-id="aabbf-110">Exiba os murals específicos chamando a função [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .</span><span class="sxs-lookup"><span data-stu-id="aabbf-110">Display particular billboards by calling the [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) function.</span></span>

 

 



