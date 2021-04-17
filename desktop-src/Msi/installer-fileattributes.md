---
description: A propriedade FileAttributes do objeto instalador retorna um número que representa os atributos de arquivo combinados para o caminho designado para um arquivo ou pasta.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Propriedade Installer. FileAttributes (Windows. Storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751439"
---
# <a name="installerfileattributes-property"></a><span data-ttu-id="3c67e-103">Propriedade Installer. FileAttributes</span><span class="sxs-lookup"><span data-stu-id="3c67e-103">Installer.FileAttributes property</span></span>

<span data-ttu-id="3c67e-104">A propriedade **FileAttributes** do objeto [**instalador**](installer-object.md) retorna um número que representa os atributos de arquivo combinados para o caminho designado para um arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="3c67e-104">The **FileAttributes** property of the [**Installer**](installer-object.md) object returns a number representing the combined file attributes for the designated path to a file or folder.</span></span>

<span data-ttu-id="3c67e-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3c67e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c67e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c67e-106">Syntax</span></span>


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a><span data-ttu-id="3c67e-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3c67e-107">Property value</span></span>

<span data-ttu-id="3c67e-108">O caminho necessário para o arquivo ou a pasta.</span><span class="sxs-lookup"><span data-stu-id="3c67e-108">The required path to the file or folder.</span></span> <span data-ttu-id="3c67e-109">Um caminho parcial assume o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="3c67e-109">A partial path assumes the current directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c67e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c67e-110">Remarks</span></span>

<span data-ttu-id="3c67e-111">A propriedade **FileAttributes** retorna os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3c67e-111">The **FileAttributes** property returns the following values.</span></span>



| <span data-ttu-id="3c67e-112">Atributo de arquivo</span><span class="sxs-lookup"><span data-stu-id="3c67e-112">File attribute</span></span>              | <span data-ttu-id="3c67e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3c67e-113">Value</span></span>      | <span data-ttu-id="3c67e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3c67e-114">Value</span></span> |
|-----------------------------|------------|-------|
| <span data-ttu-id="3c67e-115">FILE\_ATTRIBUTE\_READONLY</span><span class="sxs-lookup"><span data-stu-id="3c67e-115">FILE\_ATTRIBUTE\_READONLY</span></span>   | <span data-ttu-id="3c67e-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3c67e-116">0x00000001</span></span> | <span data-ttu-id="3c67e-117">1</span><span class="sxs-lookup"><span data-stu-id="3c67e-117">1</span></span>     |
| <span data-ttu-id="3c67e-118">FILE\_ATTRIBUTE\_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="3c67e-118">FILE\_ATTRIBUTE\_HIDDEN</span></span>     | <span data-ttu-id="3c67e-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3c67e-119">0x00000002</span></span> | <span data-ttu-id="3c67e-120">2</span><span class="sxs-lookup"><span data-stu-id="3c67e-120">2</span></span>     |
| <span data-ttu-id="3c67e-121">FILE\_ATTRIBUTE\_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="3c67e-121">FILE\_ATTRIBUTE\_SYSTEM</span></span>     | <span data-ttu-id="3c67e-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3c67e-122">0x00000004</span></span> | <span data-ttu-id="3c67e-123">4</span><span class="sxs-lookup"><span data-stu-id="3c67e-123">4</span></span>     |
| <span data-ttu-id="3c67e-124">FILE\_ATTRIBUTE\_DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="3c67e-124">FILE\_ATTRIBUTE\_DIRECTORY</span></span>  | <span data-ttu-id="3c67e-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3c67e-125">0x00000010</span></span> | <span data-ttu-id="3c67e-126">16</span><span class="sxs-lookup"><span data-stu-id="3c67e-126">16</span></span>    |
| <span data-ttu-id="3c67e-127">atributo de arquivo \_ \_ temporário</span><span class="sxs-lookup"><span data-stu-id="3c67e-127">FILE\_ATTRIBUTE\_TEMPORARY</span></span>  | <span data-ttu-id="3c67e-128">0x00000100</span><span class="sxs-lookup"><span data-stu-id="3c67e-128">0x00000100</span></span> | <span data-ttu-id="3c67e-129">256</span><span class="sxs-lookup"><span data-stu-id="3c67e-129">256</span></span>   |
| <span data-ttu-id="3c67e-130">FILE\_ATTRIBUTE\_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="3c67e-130">FILE\_ATTRIBUTE\_COMPRESSED</span></span> | <span data-ttu-id="3c67e-131">0x00000800</span><span class="sxs-lookup"><span data-stu-id="3c67e-131">0x00000800</span></span> | <span data-ttu-id="3c67e-132">2.048</span><span class="sxs-lookup"><span data-stu-id="3c67e-132">2048</span></span>  |
| <span data-ttu-id="3c67e-133">FILE\_ATTRIBUTE\_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3c67e-133">FILE\_ATTRIBUTE\_OFFLINE</span></span>    | <span data-ttu-id="3c67e-134">0x00001000</span><span class="sxs-lookup"><span data-stu-id="3c67e-134">0x00001000</span></span> | <span data-ttu-id="3c67e-135">4096</span><span class="sxs-lookup"><span data-stu-id="3c67e-135">4096</span></span>  |



 

<span data-ttu-id="3c67e-136">Retornará – 1 se o arquivo ou a pasta não existir ou não estiver acessível.</span><span class="sxs-lookup"><span data-stu-id="3c67e-136">Returns –1 if the file or folder does not exist or is not accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c67e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c67e-137">Requirements</span></span>



| <span data-ttu-id="3c67e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c67e-138">Requirement</span></span> | <span data-ttu-id="3c67e-139">Valor</span><span class="sxs-lookup"><span data-stu-id="3c67e-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c67e-140">Versão</span><span class="sxs-lookup"><span data-stu-id="3c67e-140">Version</span></span><br/> | <span data-ttu-id="3c67e-141">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3c67e-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3c67e-142">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3c67e-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3c67e-143">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c67e-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3c67e-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c67e-144">Header</span></span><br/>  | <dl> <span data-ttu-id="3c67e-145"><dt>Windows. Storage. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c67e-145"><dt>Windows.storage.h</dt></span></span> </dl>                                                                                                                                                            |
| <span data-ttu-id="3c67e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="3c67e-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c67e-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c67e-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3c67e-148">IID</span><span class="sxs-lookup"><span data-stu-id="3c67e-148">IID</span></span><br/>     | <span data-ttu-id="3c67e-149">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3c67e-149">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




