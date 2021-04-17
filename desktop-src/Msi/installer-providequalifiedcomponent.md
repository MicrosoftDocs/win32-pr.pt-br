---
description: O método ProvideQualifiedComponent do objeto do instalador retorna o caminho completo do componente e executa qualquer instalação necessária. Se necessário, esse método solicita a origem e incrementa a contagem de uso para o recurso.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Método Installer. ProvideQualifiedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752450"
---
# <a name="installerprovidequalifiedcomponent-method"></a><span data-ttu-id="afe65-104">Método Installer. ProvideQualifiedComponent</span><span class="sxs-lookup"><span data-stu-id="afe65-104">Installer.ProvideQualifiedComponent method</span></span>

<span data-ttu-id="afe65-105">O método **ProvideQualifiedComponent** do objeto do [**instalador**](installer-object.md) retorna o caminho completo do componente e executa qualquer instalação necessária.</span><span class="sxs-lookup"><span data-stu-id="afe65-105">The **ProvideQualifiedComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="afe65-106">Se necessário, esse método solicita a origem e incrementa a contagem de uso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="afe65-106">If necessary, this method prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe65-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afe65-107">Syntax</span></span>


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="afe65-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afe65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afe65-109">*Categoria*</span><span class="sxs-lookup"><span data-stu-id="afe65-109">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="afe65-110">Especifica a ID do componente solicitado.</span><span class="sxs-lookup"><span data-stu-id="afe65-110">Specifies the component ID for the requested component.</span></span> <span data-ttu-id="afe65-111">Esse pode não ser o GUID do próprio componente, mas sim um servidor que fornece a funcionalidade correta, como na coluna ComponentID da [tabela PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="afe65-111">This may not be the GUID for the component itself but rather a server that provides the correct functionality, as in the ComponentId column of the [PublishComponent table](publishcomponent-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="afe65-112">*Qualificador*</span><span class="sxs-lookup"><span data-stu-id="afe65-112">*Qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="afe65-113">Especifica um qualificador em uma lista de componentes de propaganda (da [tabela PublishComponent](publishcomponent-table.md)).</span><span class="sxs-lookup"><span data-stu-id="afe65-113">Specifies a qualifier into a list of advertising components (from [PublishComponent table](publishcomponent-table.md)).</span></span>

</dd> <dt>

<span data-ttu-id="afe65-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="afe65-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="afe65-115">Define o modo de instalação.</span><span class="sxs-lookup"><span data-stu-id="afe65-115">Defines the installation mode.</span></span> <span data-ttu-id="afe65-116">Esse parâmetro pode ser um dos valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="afe65-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="afe65-117">InstallMode</span><span class="sxs-lookup"><span data-stu-id="afe65-117">InstallMode</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="afe65-118">Significado</span><span class="sxs-lookup"><span data-stu-id="afe65-118">Meaning</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="afe65-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="afe65-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                 | <span data-ttu-id="afe65-120">Fornece o componente, executando qualquer instalação necessária.</span><span class="sxs-lookup"><span data-stu-id="afe65-120">Provides the component, performing any necessary installation.</span></span><br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="afe65-121"><dt>**msiInstallModeExisting**</dt> <dt>– 1</dt></span><span class="sxs-lookup"><span data-stu-id="afe65-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                            | <span data-ttu-id="afe65-122">Fornece o componente somente se o recurso existir; caso contrário, retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="afe65-122">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="afe65-123">Esse modo verifica a existência do arquivo de chave do componente.</span><span class="sxs-lookup"><span data-stu-id="afe65-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="afe65-124"><dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="afe65-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                                | <span data-ttu-id="afe65-125">Fornece o componente somente se o recurso existir; caso contrário, retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="afe65-125">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="afe65-126">Esse modo verifica apenas se o componente está registrado, mas não verifica a existência do arquivo de chave do componente.</span><span class="sxs-lookup"><span data-stu-id="afe65-126">This mode only checks that the component is registered but does not verify the existence of the component's key file.</span></span><br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="afe65-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="afe65-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                    | <span data-ttu-id="afe65-128">Fornece o caminho do componente somente se o recurso existir com um parâmetro InstallState de *msiInstallStateLocal*.</span><span class="sxs-lookup"><span data-stu-id="afe65-128">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="afe65-129">Isso verifica o registro do componente, mas não verifica a existência do arquivo de chave do componente.</span><span class="sxs-lookup"><span data-stu-id="afe65-129">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="afe65-130"><dt>**combinação dos sinalizadores msiReinstallMode**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="afe65-130"><dt>**combination of the msiReinstallMode flags**</dt> <dt> </dt></span></span> </dl> | <span data-ttu-id="afe65-131">Chama [**ReinstallFeature**](installer-reinstallfeature.md) para reinstalar o recurso usando esse parâmetro para o parâmetro *REINSTALLMODE* e, em seguida, fornece o componente.</span><span class="sxs-lookup"><span data-stu-id="afe65-131">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afe65-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="afe65-132">Return value</span></span>

<span data-ttu-id="afe65-133">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="afe65-133">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="afe65-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afe65-134">Requirements</span></span>



| <span data-ttu-id="afe65-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="afe65-135">Requirement</span></span> | <span data-ttu-id="afe65-136">Valor</span><span class="sxs-lookup"><span data-stu-id="afe65-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe65-137">Versão</span><span class="sxs-lookup"><span data-stu-id="afe65-137">Version</span></span><br/> | <span data-ttu-id="afe65-138">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="afe65-138">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="afe65-139">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="afe65-139">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="afe65-140">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="afe65-140">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="afe65-141">DLL</span><span class="sxs-lookup"><span data-stu-id="afe65-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="afe65-142"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afe65-142"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="afe65-143">IID</span><span class="sxs-lookup"><span data-stu-id="afe65-143">IID</span></span><br/>     | <span data-ttu-id="afe65-144">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="afe65-144">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="afe65-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="afe65-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe65-146">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="afe65-146">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




