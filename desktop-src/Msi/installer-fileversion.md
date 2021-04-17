---
description: O método FileVersion do objeto instalador retorna a cadeia de caracteres da versão ou a cadeia de caracteres do caminho especificado em path usando o formato no qual o instalador espera encontrá-las no banco de dados.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Método Installer. FileVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747971"
---
# <a name="installerfileversion-method"></a><span data-ttu-id="c966e-103">Método Installer. FileVersion</span><span class="sxs-lookup"><span data-stu-id="c966e-103">Installer.FileVersion method</span></span>

<span data-ttu-id="c966e-104">O método **FileVersion** do objeto [**instalador**](installer-object.md) retorna a cadeia de caracteres da versão ou a cadeia de caracteres do caminho especificado em *Path* usando o formato no qual o instalador espera encontrá-las no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c966e-104">The **FileVersion** method of the [**Installer**](installer-object.md) object returns the version string or language string of the path specified in *Path* using the format in which the installer expects to find them in the database.</span></span> <span data-ttu-id="c966e-105">Para versões, esta é uma cadeia de caracteres \# no \# formato ".. \# . \# ".</span><span class="sxs-lookup"><span data-stu-id="c966e-105">For versions, this is a string in "\#.\#.\#.\#" format.</span></span> <span data-ttu-id="c966e-106">Para o idioma, essa é a ID de idioma decimal.</span><span class="sxs-lookup"><span data-stu-id="c966e-106">For language, this is the decimal language ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="c966e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c966e-107">Syntax</span></span>


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="c966e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c966e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c966e-109">*Caminho*</span><span class="sxs-lookup"><span data-stu-id="c966e-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="c966e-110">Cadeia de caracteres necessária que contém o caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c966e-110">Required string containing the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="c966e-111">*Idioma*</span><span class="sxs-lookup"><span data-stu-id="c966e-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="c966e-112">Sinalizador para designar se o valor retornado é uma ID de idioma ou uma cadeia de caracteres de versão.</span><span class="sxs-lookup"><span data-stu-id="c966e-112">Flag for designating whether the returned value is a language ID or version string.</span></span> <span data-ttu-id="c966e-113">TRUE retorna o idioma; FALSE retorna a versão.</span><span class="sxs-lookup"><span data-stu-id="c966e-113">TRUE returns the language, FALSE returns the version.</span></span> <span data-ttu-id="c966e-114">Esse parâmetro é opcional, com um valor padrão de FALSE.</span><span class="sxs-lookup"><span data-stu-id="c966e-114">This parameter is optional, with a default value of FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c966e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c966e-115">Return value</span></span>

<span data-ttu-id="c966e-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c966e-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c966e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c966e-117">Requirements</span></span>



| <span data-ttu-id="c966e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c966e-118">Requirement</span></span> | <span data-ttu-id="c966e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c966e-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c966e-120">Versão</span><span class="sxs-lookup"><span data-stu-id="c966e-120">Version</span></span><br/> | <span data-ttu-id="c966e-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c966e-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c966e-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c966e-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c966e-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c966e-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c966e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c966e-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c966e-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c966e-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c966e-126">IID</span><span class="sxs-lookup"><span data-stu-id="c966e-126">IID</span></span><br/>     | <span data-ttu-id="c966e-127">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c966e-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




