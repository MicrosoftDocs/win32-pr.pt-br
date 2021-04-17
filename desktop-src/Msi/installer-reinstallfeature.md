---
description: O método ReinstallFeature do objeto do instalador reinstala recursos ou corrige problemas com os recursos instalados.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Método Installer. ReinstallFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6bac008ee7121bbcb985b9a8ff5ba02df122266
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749583"
---
# <a name="installerreinstallfeature-method"></a><span data-ttu-id="112a0-103">Método Installer. ReinstallFeature</span><span class="sxs-lookup"><span data-stu-id="112a0-103">Installer.ReinstallFeature method</span></span>

<span data-ttu-id="112a0-104">O método **ReinstallFeature** do objeto do [**instalador**](installer-object.md) reinstala recursos ou corrige problemas com os recursos instalados.</span><span class="sxs-lookup"><span data-stu-id="112a0-104">The **ReinstallFeature** method of the [**Installer**](installer-object.md) object reinstalls features or corrects problems with installed features.</span></span>

## <a name="syntax"></a><span data-ttu-id="112a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="112a0-105">Syntax</span></span>


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="112a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="112a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="112a0-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="112a0-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="112a0-108">Especifica o código do produto do produto.</span><span class="sxs-lookup"><span data-stu-id="112a0-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="112a0-109">*Recurso*</span><span class="sxs-lookup"><span data-stu-id="112a0-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="112a0-110">Especifica o recurso a ser reinstalado.</span><span class="sxs-lookup"><span data-stu-id="112a0-110">Specifies the feature to be reinstalled.</span></span> <span data-ttu-id="112a0-111">O recurso pai ou o recurso filho do recurso especificado não é reinstalado.</span><span class="sxs-lookup"><span data-stu-id="112a0-111">The parent feature or child feature of the specified feature is not reinstalled.</span></span> <span data-ttu-id="112a0-112">Para reinstalar o recurso pai ou filho, você deve chamar o método **ReinstallFeature** para cada um separadamente ou usar o método [**ReinstallProduct**](installer-reinstallproduct.md) .</span><span class="sxs-lookup"><span data-stu-id="112a0-112">To reinstall the parent or child feature, you must call the **ReinstallFeature** method for each separately or use the [**ReinstallProduct**](installer-reinstallproduct.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="112a0-113">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="112a0-113">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="112a0-114">Especifica o tipo de reinstalação.</span><span class="sxs-lookup"><span data-stu-id="112a0-114">Specifies the type of reinstallation.</span></span> <span data-ttu-id="112a0-115">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="112a0-115">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="112a0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="112a0-116">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="112a0-117">Significado</span><span class="sxs-lookup"><span data-stu-id="112a0-117">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="112a0-118"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-118"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="112a0-119">Reinstalará somente se o arquivo estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="112a0-119">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="112a0-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="112a0-121">Reinstala se o arquivo está ausente ou é uma versão mais antiga.</span><span class="sxs-lookup"><span data-stu-id="112a0-121">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="112a0-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="112a0-123">Reinstala se o arquivo está ausente ou é uma versão igual ou anterior.</span><span class="sxs-lookup"><span data-stu-id="112a0-123">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="112a0-124"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-124"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="112a0-125">Reinstala se o arquivo está ausente ou não é uma versão exata.</span><span class="sxs-lookup"><span data-stu-id="112a0-125">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="112a0-126"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-126"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="112a0-127">Verifica os executáveis de soma e reinstala se eles estiverem ausentes ou corrompidos.</span><span class="sxs-lookup"><span data-stu-id="112a0-127">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="112a0-128"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-128"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="112a0-129">Reinstala todos os arquivos, independentemente da versão.</span><span class="sxs-lookup"><span data-stu-id="112a0-129">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="112a0-130"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-130"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="112a0-131">Garante as entradas de registro obrigatórias per = user.</span><span class="sxs-lookup"><span data-stu-id="112a0-131">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="112a0-132"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-132"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="112a0-133">Garante o necessário por entradas de registro de computador.</span><span class="sxs-lookup"><span data-stu-id="112a0-133">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="112a0-134"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-134"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="112a0-135">Valida atalhos.</span><span class="sxs-lookup"><span data-stu-id="112a0-135">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="112a0-136"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-136"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="112a0-137">Usa a origem de recache para instalar o pacote.</span><span class="sxs-lookup"><span data-stu-id="112a0-137">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="112a0-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="112a0-138">Return value</span></span>

<span data-ttu-id="112a0-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="112a0-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="112a0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="112a0-140">Requirements</span></span>



| <span data-ttu-id="112a0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="112a0-141">Requirement</span></span> | <span data-ttu-id="112a0-142">Valor</span><span class="sxs-lookup"><span data-stu-id="112a0-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="112a0-143">Versão</span><span class="sxs-lookup"><span data-stu-id="112a0-143">Version</span></span><br/> | <span data-ttu-id="112a0-144">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="112a0-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="112a0-145">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="112a0-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="112a0-146">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="112a0-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="112a0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="112a0-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="112a0-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="112a0-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="112a0-149">IID</span><span class="sxs-lookup"><span data-stu-id="112a0-149">IID</span></span><br/>     | <span data-ttu-id="112a0-150">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="112a0-150">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="112a0-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="112a0-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112a0-152">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="112a0-152">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[<span data-ttu-id="112a0-153">Funções de instalação e configuração</span><span class="sxs-lookup"><span data-stu-id="112a0-153">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




