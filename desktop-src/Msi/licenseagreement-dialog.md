---
description: Essa caixa de diálogo modal exibe o contrato de licença para o usuário.
ms.assetid: 367fe264-6e08-4b40-b61b-617bb92986b7
title: Caixa de diálogo LicenseAgreement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8876f315787671ee36de42e5b86167659611a77a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812915"
---
# <a name="licenseagreement-dialog"></a><span data-ttu-id="42d4b-103">Caixa de diálogo LicenseAgreement</span><span class="sxs-lookup"><span data-stu-id="42d4b-103">LicenseAgreement Dialog</span></span>

<span data-ttu-id="42d4b-104">Essa caixa de diálogo modal exibe o contrato de licença para o usuário.</span><span class="sxs-lookup"><span data-stu-id="42d4b-104">This modal dialog box displays the license agreement to the user.</span></span> <span data-ttu-id="42d4b-105">Normalmente, a caixa de diálogo exibe o texto do contrato usando um [controle ScrollableText](scrollabletext-control.md) e um par de botões de opção que permitem que o usuário aceite ou rejeite o contrato.</span><span class="sxs-lookup"><span data-stu-id="42d4b-105">Typically the dialog box displays the text of the agreement using a [ScrollableText control](scrollabletext-control.md) and a pair of option buttons that let the user accept or reject the agreement.</span></span> <span data-ttu-id="42d4b-106">Por motivos legais, é aconselhável que nenhum botão seja apresentado ao usuário como já selecionado por padrão.</span><span class="sxs-lookup"><span data-stu-id="42d4b-106">For legal reasons it is advisable that neither button be presented to the user as already selected by default.</span></span> <span data-ttu-id="42d4b-107">Isso força o usuário a fazer uma escolha ativa.</span><span class="sxs-lookup"><span data-stu-id="42d4b-107">This forces the user to make an active choice.</span></span> <span data-ttu-id="42d4b-108">Os autores geralmente usam um [controle de botão de opção](radiobuttongroup-control.md) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="42d4b-108">Authors commonly use a [RadioButtonGroup control](radiobuttongroup-control.md) for this purpose.</span></span> <span data-ttu-id="42d4b-109">No entanto, observe que o foco em uma caixa de diálogo não é movido para um controle de grupo de botões de opção até que um dos botões no grupo tenha sido selecionado.</span><span class="sxs-lookup"><span data-stu-id="42d4b-109">Note however that the focus on a dialog box does not move to a RadioButtonGroup control until one of the buttons in the group has been selected.</span></span>

 

 



