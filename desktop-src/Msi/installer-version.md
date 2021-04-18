---
description: A Propriedade Version do objeto instalador é uma propriedade somente leitura que é a representação de cadeia de caracteres da versão atual do Windows Installer. A cadeia de caracteres é retornada no formulário a seguir.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Propriedade Installer. Version
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 29af85b8fc1afe468dc87d5516da9a528024c73a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752036"
---
# <a name="installerversion-property"></a><span data-ttu-id="80f5b-104">Propriedade Installer. Version</span><span class="sxs-lookup"><span data-stu-id="80f5b-104">Installer.Version property</span></span>

<span data-ttu-id="80f5b-105">A propriedade **version** do objeto [**instalador**](installer-object.md) é uma propriedade somente leitura que é a representação de cadeia de caracteres da versão atual do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="80f5b-105">The **Version** property of the [**Installer**](installer-object.md) object is a read-only property that is the string representation of the current version of Windows Installer.</span></span> <span data-ttu-id="80f5b-106">A cadeia de caracteres é retornada no formulário a seguir.</span><span class="sxs-lookup"><span data-stu-id="80f5b-106">The string is returned in the following form.</span></span>

<span data-ttu-id="80f5b-107">*principal*. *secundária*. *Compilar*. *Atualizar* o</span><span class="sxs-lookup"><span data-stu-id="80f5b-107">*major*.*minor*.*build*.*update*</span></span>

<span data-ttu-id="80f5b-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="80f5b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80f5b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80f5b-109">Syntax</span></span>


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a><span data-ttu-id="80f5b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="80f5b-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="80f5b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80f5b-111">Requirements</span></span>



| <span data-ttu-id="80f5b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="80f5b-112">Requirement</span></span> | <span data-ttu-id="80f5b-113">Valor</span><span class="sxs-lookup"><span data-stu-id="80f5b-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f5b-114">Versão</span><span class="sxs-lookup"><span data-stu-id="80f5b-114">Version</span></span><br/> | <span data-ttu-id="80f5b-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80f5b-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="80f5b-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="80f5b-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="80f5b-117">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="80f5b-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="80f5b-118">DLL</span><span class="sxs-lookup"><span data-stu-id="80f5b-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="80f5b-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80f5b-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="80f5b-120">IID</span><span class="sxs-lookup"><span data-stu-id="80f5b-120">IID</span></span><br/>     | <span data-ttu-id="80f5b-121">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="80f5b-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




