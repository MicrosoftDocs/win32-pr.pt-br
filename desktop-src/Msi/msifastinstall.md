---
description: A propriedade MSIFASTINSTALL pode ser usada para reduzir o tempo necessário para instalar um grande pacote de Windows Installer.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Propriedade MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748766"
---
# <a name="msifastinstall-property"></a><span data-ttu-id="39df3-103">Propriedade MSIFASTINSTALL</span><span class="sxs-lookup"><span data-stu-id="39df3-103">MSIFASTINSTALL property</span></span>

<span data-ttu-id="39df3-104">A propriedade **MSIFASTINSTALL** pode ser usada para reduzir o tempo necessário para instalar um grande pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="39df3-104">The **MSIFASTINSTALL** property can be used to reduce the time required to install a large Windows Installer package.</span></span> <span data-ttu-id="39df3-105">A propriedade pode ser definida na linha de comando ou na tabela de [Propriedades](property-table.md) para configurar as operações que o usuário ou o desenvolvedor determina não são essenciais para a instalação.</span><span class="sxs-lookup"><span data-stu-id="39df3-105">The property can be set on the command line or in the [Property](property-table.md) table to configure operations that the user or developer determines are non-essential for the installation.</span></span>

<span data-ttu-id="39df3-106">O valor da propriedade **MSIFASTINSTALL** pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="39df3-106">The value of the **MSIFASTINSTALL** property can be a combination of the following values.</span></span>



| <span data-ttu-id="39df3-107">Valor</span><span class="sxs-lookup"><span data-stu-id="39df3-107">Value</span></span> | <span data-ttu-id="39df3-108">Significado</span><span class="sxs-lookup"><span data-stu-id="39df3-108">Meaning</span></span>                                                                      |
|-------|------------------------------------------------------------------------------|
| <span data-ttu-id="39df3-109">0</span><span class="sxs-lookup"><span data-stu-id="39df3-109">0</span></span>     | <span data-ttu-id="39df3-110">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="39df3-110">Default value</span></span>                                                                |
| <span data-ttu-id="39df3-111">1</span><span class="sxs-lookup"><span data-stu-id="39df3-111">1</span></span>     | <span data-ttu-id="39df3-112">Nenhum ponto de restauração do sistema foi salvo para esta instalação.</span><span class="sxs-lookup"><span data-stu-id="39df3-112">No system restore point is saved for this installation.</span></span>                      |
| <span data-ttu-id="39df3-113">2</span><span class="sxs-lookup"><span data-stu-id="39df3-113">2</span></span>     | <span data-ttu-id="39df3-114">Execute apenas o [custo do arquivo](file-costing.md) e pule a verificação de outros custos.</span><span class="sxs-lookup"><span data-stu-id="39df3-114">Perform only [File Costing](file-costing.md) and skip checking other costs.</span></span> |
| <span data-ttu-id="39df3-115">4</span><span class="sxs-lookup"><span data-stu-id="39df3-115">4</span></span>     | <span data-ttu-id="39df3-116">Reduza a frequência das mensagens de progresso.</span><span class="sxs-lookup"><span data-stu-id="39df3-116">Reduce the frequency of progress messages.</span></span>                                   |



 

<span data-ttu-id="39df3-117">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="39df3-117">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="39df3-118">Essa propriedade está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="39df3-118">This property is available beginning with Windows Installer 5.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="39df3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39df3-119">Requirements</span></span>



| <span data-ttu-id="39df3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="39df3-120">Requirement</span></span> | <span data-ttu-id="39df3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="39df3-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39df3-122">Versão</span><span class="sxs-lookup"><span data-stu-id="39df3-122">Version</span></span><br/> | <span data-ttu-id="39df3-123">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="39df3-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="39df3-124">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="39df3-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



 

 




