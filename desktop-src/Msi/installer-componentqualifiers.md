---
description: A propriedade ComponentQualifiers é uma propriedade somente leitura que retorna um objeto StringList que enumera o conjunto de qualificadores registrados para o componente especificado.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Propriedade Installer. ComponentQualifiers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752852"
---
# <a name="installercomponentqualifiers-property"></a><span data-ttu-id="78e0d-103">Propriedade Installer. ComponentQualifiers</span><span class="sxs-lookup"><span data-stu-id="78e0d-103">Installer.ComponentQualifiers property</span></span>

<span data-ttu-id="78e0d-104">A propriedade **ComponentQualifiers** é uma propriedade somente leitura que retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de qualificadores registrados para o componente especificado.</span><span class="sxs-lookup"><span data-stu-id="78e0d-104">The **ComponentQualifiers** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of registered qualifiers for the specified component.</span></span>

<span data-ttu-id="78e0d-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="78e0d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e0d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78e0d-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a><span data-ttu-id="78e0d-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="78e0d-107">Property value</span></span>

<span data-ttu-id="78e0d-108">Um GUID de cadeia de caracteres que representa a categoria do [componente](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="78e0d-108">A string GUID that represents the category of [component](publishcomponent-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78e0d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="78e0d-109">Remarks</span></span>

<span data-ttu-id="78e0d-110">Para enumerar qualificadores, o aplicativo itera por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each.</span><span class="sxs-lookup"><span data-stu-id="78e0d-110">To enumerate qualifiers the application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="78e0d-111">Como os qualificadores não são ordenados, qualquer qualificador novo tem um índice arbitrário, o que significa que a função pode retornar qualificadores em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="78e0d-111">Because qualifiers are not ordered, any new qualifier has an arbitrary index, meaning the function can return qualifiers in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="78e0d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78e0d-112">Requirements</span></span>



| <span data-ttu-id="78e0d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="78e0d-113">Requirement</span></span> | <span data-ttu-id="78e0d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="78e0d-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e0d-115">Versão</span><span class="sxs-lookup"><span data-stu-id="78e0d-115">Version</span></span><br/> | <span data-ttu-id="78e0d-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="78e0d-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="78e0d-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="78e0d-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="78e0d-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="78e0d-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="78e0d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="78e0d-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="78e0d-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78e0d-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="78e0d-121">IID</span><span class="sxs-lookup"><span data-stu-id="78e0d-121">IID</span></span><br/>     | <span data-ttu-id="78e0d-122">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="78e0d-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="78e0d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="78e0d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e0d-124">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="78e0d-124">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




