---
description: O Windows Installer define a propriedade OriginalDatabase como o caminho do banco de dados de instalação usado para iniciar a instalação.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Propriedade OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758768"
---
# <a name="originaldatabase-property"></a><span data-ttu-id="2acaa-103">Propriedade OriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="2acaa-103">OriginalDatabase property</span></span>

<span data-ttu-id="2acaa-104">O Windows Installer define a propriedade **OriginalDatabase** como o caminho do banco de dados de instalação usado para iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="2acaa-104">The Windows Installer sets the **OriginalDatabase** property to the path of the installation database used to launch the installation.</span></span> <span data-ttu-id="2acaa-105">Se a instalação for iniciada a partir de uma linha de comando, o valor dependerá se a opção de recache de pacote (o sinalizador-v) está presente na propriedade [**REinstallmode**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="2acaa-105">If the installation is launched from a command line, the value depends on whether the recache package option (the -v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>



| <span data-ttu-id="2acaa-106">Método de instalação</span><span class="sxs-lookup"><span data-stu-id="2acaa-106">Installation Method</span></span>                                                                                                                                                                                  | <span data-ttu-id="2acaa-107">Valor de OriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="2acaa-107">OriginalDatabase Value</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="2acaa-108">Qualquer instalação iniciada invocando o caminho do pacote de instalação (arquivo. msi).</span><span class="sxs-lookup"><span data-stu-id="2acaa-108">Any installation launched by invoking the path of the installation package (.msi file).</span></span>                                                                                                              | <span data-ttu-id="2acaa-109">Caminho para o pacote de instalação (arquivo. msi).</span><span class="sxs-lookup"><span data-stu-id="2acaa-109">Path to the installation package (.msi file).</span></span> |
| <span data-ttu-id="2acaa-110">Instalação iniciada a partir de uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="2acaa-110">Installation launched from a command line.</span></span> <span data-ttu-id="2acaa-111">A instalação não é iniciada a partir de um caminho de pacote.</span><span class="sxs-lookup"><span data-stu-id="2acaa-111">The installation is not launched from a package path.</span></span> <span data-ttu-id="2acaa-112">A opção de recache (sinalizador-v) está presente na propriedade [**REinstallmode**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="2acaa-112">The recache option (-v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>     | <span data-ttu-id="2acaa-113">Caminho para o banco de dados na origem.</span><span class="sxs-lookup"><span data-stu-id="2acaa-113">Path to the database on the source.</span></span>           |
| <span data-ttu-id="2acaa-114">Instalação iniciada a partir de uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="2acaa-114">Installation launched from a command line.</span></span> <span data-ttu-id="2acaa-115">A instalação não é iniciada a partir de um caminho de pacote.</span><span class="sxs-lookup"><span data-stu-id="2acaa-115">The installation is not launched from a package path.</span></span> <span data-ttu-id="2acaa-116">A opção de recache (sinalizador-v) não está presente na propriedade [**REinstallmode**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="2acaa-116">The recache option (-v flag) is not present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> | <span data-ttu-id="2acaa-117">Caminho para o banco de dados armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="2acaa-117">Path to the cached database.</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="2acaa-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2acaa-118">Remarks</span></span>

<span data-ttu-id="2acaa-119">Durante uma instalação pela primeira vez, uma ação personalizada sequenciada antes da [ação resolver](resolvesource-action.md) pode usar a propriedade **OriginalDatabase** para determinar o local da origem da instalação.</span><span class="sxs-lookup"><span data-stu-id="2acaa-119">During a first time installation, a custom action sequenced before the [ResolveSource action](resolvesource-action.md) can use the **OriginalDatabase** property to determine the location of the installation source.</span></span>

## <a name="requirements"></a><span data-ttu-id="2acaa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2acaa-120">Requirements</span></span>



| <span data-ttu-id="2acaa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2acaa-121">Requirement</span></span> | <span data-ttu-id="2acaa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2acaa-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2acaa-123">Versão</span><span class="sxs-lookup"><span data-stu-id="2acaa-123">Version</span></span><br/> | <span data-ttu-id="2acaa-124">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2acaa-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2acaa-125">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2acaa-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2acaa-126">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2acaa-126">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2acaa-127">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2acaa-127">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2acaa-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2acaa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2acaa-129">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2acaa-129">Properties</span></span>](properties.md)
</dt> </dl>

 

 




