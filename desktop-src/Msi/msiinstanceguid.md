---
description: A presença da propriedade MSIINSTANCEGUID indica que um código de produto&\# 8211; a alteração da transformação está registrada para o produto.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Propriedade MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768727"
---
# <a name="msiinstanceguid-property"></a><span data-ttu-id="ce90c-103">Propriedade MSIINSTANCEGUID</span><span class="sxs-lookup"><span data-stu-id="ce90c-103">MSIINSTANCEGUID property</span></span>

<span data-ttu-id="ce90c-104">A presença da propriedade **MSIINSTANCEGUID** indica que um código de produto – alteração de transformação está registrado para o produto.</span><span class="sxs-lookup"><span data-stu-id="ce90c-104">The presence of the **MSIINSTANCEGUID** property indicates that a product code–changing transform is registered to the product.</span></span> <span data-ttu-id="ce90c-105">O valor da propriedade **MSIINSTANCEGUID** especifica qual instância de um produto deve ser usada para instalação.</span><span class="sxs-lookup"><span data-stu-id="ce90c-105">The value of the **MSIINSTANCEGUID** property specifies which instance of a product is to be used for installation.</span></span> <span data-ttu-id="ce90c-106">A propriedade **MSIINSTANCEGUID** só pode fazer referência a um produto que já tenha sido instalado com uma transformação de instância.</span><span class="sxs-lookup"><span data-stu-id="ce90c-106">The **MSIINSTANCEGUID** property can only reference a product that has already been installed with an instance transform.</span></span>

<span data-ttu-id="ce90c-107">As transformações de instância são código do produto – alterando transformações disponíveis com o instalador em execução no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce90c-107">Instance transforms are product code–changing transforms available with the installer running on either Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ce90c-108">Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="ce90c-108">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce90c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce90c-109">Requirements</span></span>



| <span data-ttu-id="ce90c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce90c-110">Requirement</span></span> | <span data-ttu-id="ce90c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ce90c-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce90c-112">Versão</span><span class="sxs-lookup"><span data-stu-id="ce90c-112">Version</span></span><br/> | <span data-ttu-id="ce90c-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ce90c-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ce90c-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce90c-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ce90c-115">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce90c-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ce90c-116">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ce90c-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce90c-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce90c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce90c-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce90c-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ce90c-119">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="ce90c-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




