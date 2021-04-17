---
description: O método ReinstallProduct do objeto do instalador reinstala um produto ou corrige problemas de instalação em um produto instalado.
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: Método Installer. ReinstallProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1570f5a0dc607b4a011a5b4276a243c59a64392d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748771"
---
# <a name="installerreinstallproduct-method"></a><span data-ttu-id="2da96-103">Método Installer. ReinstallProduct</span><span class="sxs-lookup"><span data-stu-id="2da96-103">Installer.ReinstallProduct method</span></span>

<span data-ttu-id="2da96-104">O método **ReinstallProduct** do objeto do [**instalador**](installer-object.md) reinstala um produto ou corrige problemas de instalação em um produto instalado.</span><span class="sxs-lookup"><span data-stu-id="2da96-104">The **ReinstallProduct** method of the [**Installer**](installer-object.md) object reinstalls a product or corrects installation problems in an installed product.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da96-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2da96-105">Syntax</span></span>


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="2da96-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2da96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da96-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="2da96-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="2da96-108">Especifica o código do produto do produto.</span><span class="sxs-lookup"><span data-stu-id="2da96-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="2da96-109">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="2da96-109">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="2da96-110">Especifica o tipo de reinstalação.</span><span class="sxs-lookup"><span data-stu-id="2da96-110">Specifies the type of reinstallation.</span></span> <span data-ttu-id="2da96-111">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2da96-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="2da96-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2da96-112">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="2da96-113">Significado</span><span class="sxs-lookup"><span data-stu-id="2da96-113">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="2da96-114"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-114"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="2da96-115">Reinstalará somente se o arquivo estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="2da96-115">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="2da96-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="2da96-117">Reinstala se o arquivo está ausente ou é uma versão mais antiga.</span><span class="sxs-lookup"><span data-stu-id="2da96-117">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="2da96-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="2da96-119">Reinstala se o arquivo está ausente ou é uma versão igual ou anterior.</span><span class="sxs-lookup"><span data-stu-id="2da96-119">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="2da96-120"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-120"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="2da96-121">Reinstala se o arquivo está ausente ou não é uma versão exata.</span><span class="sxs-lookup"><span data-stu-id="2da96-121">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="2da96-122"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-122"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="2da96-123">Verifica os executáveis de soma e reinstala se eles estiverem ausentes ou corrompidos.</span><span class="sxs-lookup"><span data-stu-id="2da96-123">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="2da96-124"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-124"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="2da96-125">Reinstala todos os arquivos, independentemente da versão.</span><span class="sxs-lookup"><span data-stu-id="2da96-125">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="2da96-126"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-126"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="2da96-127">Garante as entradas de registro obrigatórias per = user.</span><span class="sxs-lookup"><span data-stu-id="2da96-127">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="2da96-128"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-128"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="2da96-129">Garante o necessário por entradas de registro de computador.</span><span class="sxs-lookup"><span data-stu-id="2da96-129">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="2da96-130"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-130"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="2da96-131">Valida atalhos.</span><span class="sxs-lookup"><span data-stu-id="2da96-131">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="2da96-132"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-132"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="2da96-133">Usa a origem de recache para instalar o pacote.</span><span class="sxs-lookup"><span data-stu-id="2da96-133">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da96-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2da96-134">Return value</span></span>

<span data-ttu-id="2da96-135">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2da96-135">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da96-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2da96-136">Requirements</span></span>



| <span data-ttu-id="2da96-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da96-137">Requirement</span></span> | <span data-ttu-id="2da96-138">Valor</span><span class="sxs-lookup"><span data-stu-id="2da96-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da96-139">Versão</span><span class="sxs-lookup"><span data-stu-id="2da96-139">Version</span></span><br/> | <span data-ttu-id="2da96-140">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2da96-140">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2da96-141">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2da96-141">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2da96-142">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2da96-142">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2da96-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2da96-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="2da96-144"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2da96-144"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2da96-145">IID</span><span class="sxs-lookup"><span data-stu-id="2da96-145">IID</span></span><br/>     | <span data-ttu-id="2da96-146">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2da96-146">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="2da96-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="2da96-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da96-148">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="2da96-148">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[<span data-ttu-id="2da96-149">Funções de instalação e configuração</span><span class="sxs-lookup"><span data-stu-id="2da96-149">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




