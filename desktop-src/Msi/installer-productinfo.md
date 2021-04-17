---
description: A propriedade ProductInfo é uma propriedade somente leitura que retorna o valor do atributo especificado para um produto instalado ou publicado.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Propriedade Installer. ProductInfo (Oemupgex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748773"
---
# <a name="installerproductinfo-property"></a><span data-ttu-id="0453e-103">Propriedade Installer. ProductInfo</span><span class="sxs-lookup"><span data-stu-id="0453e-103">Installer.ProductInfo property</span></span>

<span data-ttu-id="0453e-104">A propriedade **ProductInfo** é uma propriedade somente leitura que retorna o valor do atributo especificado para um produto instalado ou publicado.</span><span class="sxs-lookup"><span data-stu-id="0453e-104">The **ProductInfo** property is a read-only property that returns the value of the specified attribute for an installed or published product.</span></span>

<span data-ttu-id="0453e-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0453e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0453e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0453e-106">Syntax</span></span>


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a><span data-ttu-id="0453e-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0453e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0453e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0453e-108">Remarks</span></span>

<span data-ttu-id="0453e-109">A propriedade **ProductInfo** ("LocalPackage") não retorna necessariamente um caminho para o pacote armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="0453e-109">The **ProductInfo** property ("LocalPackage") does not necessarily return a path to the cached package.</span></span> <span data-ttu-id="0453e-110">As instalações do modo de manutenção não devem ser invocadas do LocalPackage.</span><span class="sxs-lookup"><span data-stu-id="0453e-110">Maintenance mode installations should be not be invoked from the LocalPackage.</span></span> <span data-ttu-id="0453e-111">O pacote armazenado em cache é apenas para usos internos.</span><span class="sxs-lookup"><span data-stu-id="0453e-111">The cached package is for internal uses only.</span></span>

## <a name="requirements"></a><span data-ttu-id="0453e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0453e-112">Requirements</span></span>



| <span data-ttu-id="0453e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0453e-113">Requirement</span></span> | <span data-ttu-id="0453e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0453e-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0453e-115">Versão</span><span class="sxs-lookup"><span data-stu-id="0453e-115">Version</span></span><br/> | <span data-ttu-id="0453e-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0453e-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0453e-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0453e-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0453e-118">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0453e-118">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="0453e-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0453e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0453e-120"><dt>Oemupgex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0453e-120"><dt>Oemupgex.h</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="0453e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0453e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="0453e-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0453e-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="0453e-123">IID</span><span class="sxs-lookup"><span data-stu-id="0453e-123">IID</span></span><br/>     | <span data-ttu-id="0453e-124">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0453e-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="0453e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0453e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0453e-126">**MsiGetProductInfo**</span><span class="sxs-lookup"><span data-stu-id="0453e-126">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="0453e-127">**MsiGetUserInfo**</span><span class="sxs-lookup"><span data-stu-id="0453e-127">**MsiGetUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[<span data-ttu-id="0453e-128">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="0453e-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




