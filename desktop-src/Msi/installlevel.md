---
description: A propriedade INSTALLLEVEL é o nível inicial no qual os recursos são selecionados &\# 0034; em&\# 0034; para instalação por padrão.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Propriedade INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810327"
---
# <a name="installlevel-property"></a><span data-ttu-id="8bdee-103">Propriedade INSTALLLEVEL</span><span class="sxs-lookup"><span data-stu-id="8bdee-103">INSTALLLEVEL property</span></span>

<span data-ttu-id="8bdee-104">A propriedade **INSTALLLEVEL** é o nível inicial no qual os recursos são selecionados "ativados" para instalação por padrão.</span><span class="sxs-lookup"><span data-stu-id="8bdee-104">The **INSTALLLEVEL** property is the initial level at which features are selected "ON" for installation by default.</span></span> <span data-ttu-id="8bdee-105">Um recurso será instalado somente se o valor no campo nível da tabela de [recursos](feature-table.md) for menor ou igual ao valor de INSTALLLEVEL atual.</span><span class="sxs-lookup"><span data-stu-id="8bdee-105">A feature is installed only if the value in the Level field of the [Feature table](feature-table.md) is less than or equal to the current INSTALLLEVEL value.</span></span> <span data-ttu-id="8bdee-106">O nível de instalação para qualquer instalação é especificado pela propriedade **INSTALLLEVEL** e pode ser um integral de 1 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="8bdee-106">The installation level for any installation is specified by the **INSTALLLEVEL** property, and can be an integral from 1 to 32,767.</span></span> <span data-ttu-id="8bdee-107">Para obter mais informações sobre os níveis de instalação, consulte [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8bdee-107">For further discussion of installation levels, see [Feature Table](feature-table.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="8bdee-108">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="8bdee-108">Default Value</span></span>

<span data-ttu-id="8bdee-109">Se nenhum valor for especificado, o nível de instalação padrão será 1.</span><span class="sxs-lookup"><span data-stu-id="8bdee-109">If no value is specified, the install level defaults to 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bdee-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bdee-110">Remarks</span></span>

<span data-ttu-id="8bdee-111">O nível de instalação especificado pela propriedade **INSTALLLEVEL** pode ser substituído pelas seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="8bdee-111">The installation level specified by the **INSTALLLEVEL** property can be overridden by the following properties:</span></span>

-   [<span data-ttu-id="8bdee-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8bdee-112">**ADDLOCAL**</span></span>](addlocal.md)
-   [<span data-ttu-id="8bdee-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="8bdee-113">**ADDSOURCE**</span></span>](addsource.md)
-   [<span data-ttu-id="8bdee-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8bdee-114">**ADDDEFAULT**</span></span>](adddefault.md)
-   [<span data-ttu-id="8bdee-115">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8bdee-115">**COMPADDLOCAL**</span></span>](compaddlocal.md)
-   [<span data-ttu-id="8bdee-116">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8bdee-116">**COMPADDSOURCE**</span></span>](compaddsource.md)
-   [<span data-ttu-id="8bdee-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8bdee-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="8bdee-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8bdee-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="8bdee-119">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="8bdee-119">**REMOVE**</span></span>](remove.md)
-   [<span data-ttu-id="8bdee-120">**Install**</span><span class="sxs-lookup"><span data-stu-id="8bdee-120">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="8bdee-121">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="8bdee-121">**ADVERTISE**</span></span>](advertise.md)

<span data-ttu-id="8bdee-122">Por exemplo, a configuração de ADDLOCAL = ALL instala todos os recursos localmente, independentemente do valor da propriedade **INSTALLLEVEL** .</span><span class="sxs-lookup"><span data-stu-id="8bdee-122">For example, setting ADDLOCAL=ALL installs all features locally regardless of the value of the **INSTALLLEVEL** property.</span></span> <span data-ttu-id="8bdee-123">Se o valor da coluna nível na tabela de [recursos](feature-table.md) for 0, esse recurso não será instalado e não exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8bdee-123">If the value of the Level column in the [Feature table](feature-table.md) is 0, that feature is not installed and not displayed in the UI.</span></span>

<span data-ttu-id="8bdee-124">Um administrador pode desabilitar permanentemente um recurso aplicando uma transformação de personalização que define um 0 na coluna nível para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="8bdee-124">An administrator can permanently disable a feature by applying a customization transform that sets a 0 in the Level column for that feature.</span></span> <span data-ttu-id="8bdee-125">O aplicativo da transformação personalização impede a instalação e a exibição do recurso, mesmo que o usuário selecione uma instalação completa usando a interface do usuário ou definindo ADDLOCAL como ALL na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="8bdee-125">The application of the customization transform prevents the installation and display of the feature even if the user selects a complete installation using the UI or by setting ADDLOCAL to ALL on the command line.</span></span> <span data-ttu-id="8bdee-126">Consulte [um exemplo de transformação personalização](a-customization-transform-example.md).</span><span class="sxs-lookup"><span data-stu-id="8bdee-126">See [A Customization Transform Example](a-customization-transform-example.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bdee-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bdee-127">Requirements</span></span>



| <span data-ttu-id="8bdee-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bdee-128">Requirement</span></span> | <span data-ttu-id="8bdee-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8bdee-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bdee-130">Versão</span><span class="sxs-lookup"><span data-stu-id="8bdee-130">Version</span></span><br/> | <span data-ttu-id="8bdee-131">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8bdee-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8bdee-132">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8bdee-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8bdee-133">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8bdee-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8bdee-134">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8bdee-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8bdee-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bdee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bdee-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8bdee-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




