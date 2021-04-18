---
description: A propriedade ProductCode é um identificador exclusivo para a versão específica do produto, representada como um GUID de cadeia de caracteres, por exemplo &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Propriedade ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778557"
---
# <a name="productcode-property"></a><span data-ttu-id="8e3f0-103">Propriedade ProductCode</span><span class="sxs-lookup"><span data-stu-id="8e3f0-103">ProductCode property</span></span>

<span data-ttu-id="8e3f0-104">A propriedade **ProductCode** é um identificador exclusivo para a versão específica do produto, representada como um [GUID](guid.md)de cadeia de caracteres, por exemplo " {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="8e3f0-104">The **ProductCode** property is a unique identifier for the particular product release, represented as a string [GUID](guid.md), for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="8e3f0-105">As letras usadas neste GUID devem estar em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-105">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="8e3f0-106">Essa ID deve variar para diferentes versões e idiomas.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-106">This ID must vary for different versions and languages.</span></span>

<span data-ttu-id="8e3f0-107">Uma atualização de produto que atualiza um produto em um produto totalmente novo também deve alterar o código do produto.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-107">A product upgrade that updates a product into an entirely new product must also change the product code.</span></span> <span data-ttu-id="8e3f0-108">As versões de 32 bits e 64 bits do pacote de um aplicativo devem ser atribuídas a códigos de produtos diferentes.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-108">The 32-bit and 64-bit versions of an application's package must be assigned different product codes.</span></span>

<span data-ttu-id="8e3f0-109">O **ProductCode** é anunciado como uma propriedade de produto e é o método principal de especificar o produto.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-109">The **ProductCode** is advertised as a product property, and is the primary method of specifying the product.</span></span> <span data-ttu-id="8e3f0-110">Essa propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-110">This property is REQUIRED.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e3f0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e3f0-111">Requirements</span></span>



| <span data-ttu-id="8e3f0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e3f0-112">Requirement</span></span> | <span data-ttu-id="8e3f0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8e3f0-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3f0-114">Versão</span><span class="sxs-lookup"><span data-stu-id="8e3f0-114">Version</span></span><br/> | <span data-ttu-id="8e3f0-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8e3f0-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8e3f0-117">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8e3f0-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8e3f0-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e3f0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e3f0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3f0-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8e3f0-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




