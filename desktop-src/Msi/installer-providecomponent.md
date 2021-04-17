---
description: O método ProvideComponent do objeto do instalador retorna o caminho completo do componente e executa qualquer instalação necessária.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Método Installer. ProvideComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751438"
---
# <a name="installerprovidecomponent-method"></a><span data-ttu-id="00031-103">Método Installer. ProvideComponent</span><span class="sxs-lookup"><span data-stu-id="00031-103">Installer.ProvideComponent method</span></span>

<span data-ttu-id="00031-104">O método **ProvideComponent** do objeto do [**instalador**](installer-object.md) retorna o caminho completo do componente e executa qualquer instalação necessária.</span><span class="sxs-lookup"><span data-stu-id="00031-104">The **ProvideComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="00031-105">Se necessário, o método **ProvideComponent** do objeto [**instalador**](installer-object.md) solicita a origem e incrementa a contagem de uso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="00031-105">If necessary, the **ProvideComponent** method of the [**Installer**](installer-object.md) object prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="00031-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00031-106">Syntax</span></span>


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="00031-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00031-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00031-108">*Product*</span><span class="sxs-lookup"><span data-stu-id="00031-108">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="00031-109">Especifica o código do produto do produto.</span><span class="sxs-lookup"><span data-stu-id="00031-109">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="00031-110">*Recurso*</span><span class="sxs-lookup"><span data-stu-id="00031-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="00031-111">Especifica a ID do recurso que contém o componente.</span><span class="sxs-lookup"><span data-stu-id="00031-111">Specifies the feature ID of the feature containing the component.</span></span>

</dd> <dt>

<span data-ttu-id="00031-112">*Componente*</span><span class="sxs-lookup"><span data-stu-id="00031-112">*Component*</span></span> 
</dt> <dd>

<span data-ttu-id="00031-113">Especifica o código do componente.</span><span class="sxs-lookup"><span data-stu-id="00031-113">Specifies the component code.</span></span>

</dd> <dt>

<span data-ttu-id="00031-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="00031-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="00031-115">Define o modo de instalação.</span><span class="sxs-lookup"><span data-stu-id="00031-115">Defines the installation mode.</span></span> <span data-ttu-id="00031-116">Esse parâmetro pode ser um dos valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="00031-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="00031-117">Nome</span><span class="sxs-lookup"><span data-stu-id="00031-117">Name</span></span>                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="00031-118">Significado</span><span class="sxs-lookup"><span data-stu-id="00031-118">Meaning</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="00031-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="00031-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                | <span data-ttu-id="00031-120">Fornece o caminho do componente, executando qualquer instalação, se necessário.</span><span class="sxs-lookup"><span data-stu-id="00031-120">Provides the component path, performing any installation, if necessary.</span></span><br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="00031-121"><dt>**msiInstallModeExisting**</dt> <dt>– 1</dt></span><span class="sxs-lookup"><span data-stu-id="00031-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                           | <span data-ttu-id="00031-122">Fornece o caminho do componente somente se o recurso existir; caso contrário, retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="00031-122">Provides the component path only if the feature exists; otherwise, returns an empty string.</span></span> <span data-ttu-id="00031-123">Esse modo verifica a existência do arquivo de chave do componente.</span><span class="sxs-lookup"><span data-stu-id="00031-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="00031-124"><dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="00031-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                               | <span data-ttu-id="00031-125">Fornece o caminho do componente somente se o recurso existir.</span><span class="sxs-lookup"><span data-stu-id="00031-125">Provides the component path only if the feature exists.</span></span> <span data-ttu-id="00031-126">Caso contrário, retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="00031-126">Otherwise, returns an empty string.</span></span> <span data-ttu-id="00031-127">Esse modo verifica o registro do componente, mas não verifica a existência do arquivo de chave do componente.</span><span class="sxs-lookup"><span data-stu-id="00031-127">This mode checks the component's registration but does not verify the existence of the component's key file.</span></span><br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="00031-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="00031-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                   | <span data-ttu-id="00031-129">Fornece o caminho do componente somente se o recurso existir com um parâmetro InstallState de *msiInstallStateLocal*.</span><span class="sxs-lookup"><span data-stu-id="00031-129">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="00031-130">Isso verifica o registro do componente, mas não verifica a existência do arquivo de chave do componente.</span><span class="sxs-lookup"><span data-stu-id="00031-130">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="00031-131"><dt>**combinação dos sinalizadores msiReinstallMode**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="00031-131"><dt>**combination of the msiReinstallMode flags**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="00031-132">Chama [**ReinstallFeature**](installer-reinstallfeature.md) para reinstalar o recurso usando esse parâmetro para o parâmetro *REINSTALLMODE* e, em seguida, fornece o componente.</span><span class="sxs-lookup"><span data-stu-id="00031-132">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00031-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00031-133">Return value</span></span>

<span data-ttu-id="00031-134">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="00031-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00031-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="00031-135">Remarks</span></span>

<span data-ttu-id="00031-136">O método **ProvideComponent** combina a funcionalidade de [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md)e [**ComponentPath**](installer-componentpath.md).</span><span class="sxs-lookup"><span data-stu-id="00031-136">The **ProvideComponent** method combines the functionality of [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md), and [**ComponentPath**](installer-componentpath.md).</span></span> <span data-ttu-id="00031-137">O método **ProvideComponent** simplifica a sequência de chamada, mas também incrementa a contagem de uso e deve ser usado com cautela para evitar contagens de uso imprecisas.</span><span class="sxs-lookup"><span data-stu-id="00031-137">The **ProvideComponent** method simplifies the calling sequence, but it also increments the usage count and should be used with caution to prevent inaccurate usage counts.</span></span> <span data-ttu-id="00031-138">O método **ProvideComponent** também fornece menos flexibilidade do que uma série de chamadas individuais para os métodos e propriedades mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="00031-138">The **ProvideComponent** method also provides less flexibility than a series of individual calls to the methods and properties previously mentioned.</span></span>

<span data-ttu-id="00031-139">Se o aplicativo estiver se recuperando de uma situação inesperada, o aplicativo provavelmente já chamou [**UseFeature**](installer-usefeature.md) e incrementou a contagem de uso.</span><span class="sxs-lookup"><span data-stu-id="00031-139">If the application is recovering from an unexpected situation, the application has probably already called [**UseFeature**](installer-usefeature.md) and incremented the usage count.</span></span> <span data-ttu-id="00031-140">Nesse caso, o aplicativo deve evitar incrementar a contagem de uso chamando o método [**ConfigureFeature**](installer-configurefeature.md) em vez do método **ProvideComponent** .</span><span class="sxs-lookup"><span data-stu-id="00031-140">In this case, the application should avoid incrementing the usage count by calling the [**ConfigureFeature**](installer-configurefeature.md) method instead of the **ProvideComponent** method.</span></span>

<span data-ttu-id="00031-141">A opção msiInstallModeExisting não pode ser usada em combinação com sinalizadores msiReinstallMode.</span><span class="sxs-lookup"><span data-stu-id="00031-141">The msiInstallModeExisting option cannot be used in combination with msiReinstallMode flags.</span></span>

## <a name="requirements"></a><span data-ttu-id="00031-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00031-142">Requirements</span></span>



| <span data-ttu-id="00031-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="00031-143">Requirement</span></span> | <span data-ttu-id="00031-144">Valor</span><span class="sxs-lookup"><span data-stu-id="00031-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00031-145">Versão</span><span class="sxs-lookup"><span data-stu-id="00031-145">Version</span></span><br/> | <span data-ttu-id="00031-146">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="00031-146">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="00031-147">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="00031-147">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="00031-148">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="00031-148">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="00031-149">DLL</span><span class="sxs-lookup"><span data-stu-id="00031-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="00031-150"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00031-150"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="00031-151">IID</span><span class="sxs-lookup"><span data-stu-id="00031-151">IID</span></span><br/>     | <span data-ttu-id="00031-152">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="00031-152">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="00031-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="00031-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00031-154">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="00031-154">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




