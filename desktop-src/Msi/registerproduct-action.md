---
description: A ação RegisterProduct registra as informações do produto com o instalador e com adicionar/remover programas. Além disso, essa ação armazena o pacote de banco de dados Windows Installer no computador local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Ação RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770178"
---
# <a name="registerproduct-action"></a><span data-ttu-id="3c608-104">Ação RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="3c608-104">RegisterProduct Action</span></span>

<span data-ttu-id="3c608-105">A ação RegisterProduct registra as informações do produto com o instalador e com adicionar/remover programas.</span><span class="sxs-lookup"><span data-stu-id="3c608-105">The RegisterProduct action registers the product information with the installer and with Add/Remove Programs.</span></span> <span data-ttu-id="3c608-106">Além disso, essa ação armazena o pacote de banco de dados Windows Installer no computador local.</span><span class="sxs-lookup"><span data-stu-id="3c608-106">Additionally, this action stores the Windows Installer database package on the local computer.</span></span>

<span data-ttu-id="3c608-107">A ação RegisterProduct configura os controles exibidos por adicionar/remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="3c608-107">The RegisterProduct action configures the controls displayed by the Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="3c608-108">Para obter mais informações, consulte [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="3c608-108">For more information, see [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3c608-109">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="3c608-109">Sequence Restrictions</span></span>

<span data-ttu-id="3c608-110">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="3c608-110">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3c608-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="3c608-111">ActionData Messages</span></span>



| <span data-ttu-id="3c608-112">Campo</span><span class="sxs-lookup"><span data-stu-id="3c608-112">Field</span></span> | <span data-ttu-id="3c608-113">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="3c608-113">Description of action data</span></span>            |
|-------|---------------------------------------|
| <span data-ttu-id="3c608-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3c608-114">\[1\]</span></span> | <span data-ttu-id="3c608-115">Informações sobre o produto registrado.</span><span class="sxs-lookup"><span data-stu-id="3c608-115">Information about registered product.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3c608-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c608-116">Remarks</span></span>

<span data-ttu-id="3c608-117">A ação RegisterProduct não é executada durante a instalação em um ponto de instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="3c608-117">The RegisterProduct action is not performed during installation to an administrative installation point.</span></span>

 

 



