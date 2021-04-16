---
description: A propriedade de resumo contagem de páginas contém a versão mínima do instalador exigida pelo pacote de instalação.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Propriedade de Resumo de contagem de páginas
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749993"
---
# <a name="page-count-summary-property"></a><span data-ttu-id="4f8a4-103">Propriedade de Resumo de contagem de páginas</span><span class="sxs-lookup"><span data-stu-id="4f8a4-103">Page Count Summary property</span></span>

<span data-ttu-id="4f8a4-104">A propriedade de **Resumo contagem de páginas** contém a versão mínima do instalador exigida pelo pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-104">The **Page Count Summary** property contains the minimum installer version required by the installation package.</span></span> <span data-ttu-id="4f8a4-105">Para um mínimo de Windows Installer 2,0, essa propriedade deve ser definida como o inteiro 200.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-105">For a minimum of Windows Installer 2.0, this property must be set to the integer 200.</span></span> <span data-ttu-id="4f8a4-106">Para um mínimo de Windows Installer 3,0, essa propriedade deve ser definida como o inteiro 300.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-106">For a minimum of Windows Installer 3.0, this property must be set to the integer 300.</span></span> <span data-ttu-id="4f8a4-107">Para um mínimo de Windows Installer 3,1, essa propriedade deve ser definida como 301.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-107">For a minimum of Windows Installer 3.1, this property must be set to 301.</span></span> <span data-ttu-id="4f8a4-108">Para um mínimo de Windows Installer 4,5, essa propriedade deve ser definida como 405.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-108">For a minimum of Windows Installer 4.5, this property must be set to 405.</span></span> <span data-ttu-id="4f8a4-109">Para um mínimo de Windows Installer 5,0, essa propriedade deve ser definida como 500.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-109">For a minimum of Windows Installer 5.0, this property must be set to 500.</span></span>

<span data-ttu-id="4f8a4-110">Para [pacotes de Windows Installer de 64 bits](64-bit-windows-installer-packages.md), essa propriedade deve ser definida como o inteiro 200 ou superior.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-110">For [64-bit Windows Installer Packages](64-bit-windows-installer-packages.md), this property must be set to the integer 200 or greater.</span></span> <span data-ttu-id="4f8a4-111">Para pacotes de Windows Installer de 64 bits na plataforma Arm64, essa propriedade deve ser definida como o inteiro 500 ou superior.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-111">For 64-bit Windows Installer Packages on the Arm64 platform, this property must be set to the integer 500 or greater.</span></span>

<span data-ttu-id="4f8a4-112">Para um pacote de transformação, a propriedade de **Resumo contagem de páginas** contém a versão mínima do instalador necessária para processar a transformação.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-112">For a transform package, the **Page Count Summary** property contains the minimum installer version required to process the transform.</span></span> <span data-ttu-id="4f8a4-113">Defina como o maior dos dois valores de propriedade de **Resumo de contagem de páginas** que pertencem aos bancos de dados usados para gerar a transformação.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-113">Set to the greater of the two **Page Count Summary** property values that belong to the databases used to generate the transform.</span></span>

<span data-ttu-id="4f8a4-114">Para um pacote de patch, a propriedade de **Resumo contagem de páginas** é definida como NULL.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-114">For a patch package, the **Page Count Summary** property is set to Null.</span></span>

<span data-ttu-id="4f8a4-115">Essa propriedade de resumo é necessária.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-115">This summary property is required.</span></span>

<span data-ttu-id="4f8a4-116">Essa propriedade pode ser usada para criar um pacote que pode ser instalado somente pela versão mínima ou posterior especificada do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-116">This property can be used to author a package that can be installed only by the specified minimum or later version of the Windows Installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f8a4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f8a4-117">Requirements</span></span>



| <span data-ttu-id="4f8a4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f8a4-118">Requirement</span></span> | <span data-ttu-id="4f8a4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4f8a4-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8a4-120">Versão</span><span class="sxs-lookup"><span data-stu-id="4f8a4-120">Version</span></span><br/> | <span data-ttu-id="4f8a4-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4f8a4-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4f8a4-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4f8a4-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f8a4-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f8a4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f8a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8a4-125">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="4f8a4-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




