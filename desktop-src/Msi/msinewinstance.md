---
description: A propriedade MSINEWINSTANCE indica a instalação de uma nova instância de um produto com transformações de instância.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Propriedade MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753261"
---
# <a name="msinewinstance-property"></a><span data-ttu-id="97a32-103">Propriedade MSINEWINSTANCE</span><span class="sxs-lookup"><span data-stu-id="97a32-103">MSINEWINSTANCE property</span></span>

<span data-ttu-id="97a32-104">A propriedade **MSINEWINSTANCE** indica a instalação de uma nova instância de um produto com transformações de instância.</span><span class="sxs-lookup"><span data-stu-id="97a32-104">The **MSINEWINSTANCE** property indicates the installation of a new instance of a product with instance transforms.</span></span> <span data-ttu-id="97a32-105">Essa propriedade dá suporte a várias instâncias por meio do código do produto – alterando transformações.</span><span class="sxs-lookup"><span data-stu-id="97a32-105">This property supports multiple instances through product code–changing transforms.</span></span> <span data-ttu-id="97a32-106">O valor dessa propriedade é 1.</span><span class="sxs-lookup"><span data-stu-id="97a32-106">The value of this property is 1.</span></span> <span data-ttu-id="97a32-107">A presença dessa propriedade na linha de comando requer que a propriedade [**TRANSformações**](transforms.md) também esteja presente.</span><span class="sxs-lookup"><span data-stu-id="97a32-107">The presence of this property on the command line requires that the [**TRANSFORMS**](transforms.md) property also be present.</span></span> <span data-ttu-id="97a32-108">A primeira transformação listada em **TRANSformações** deve ser uma transformação de instância.</span><span class="sxs-lookup"><span data-stu-id="97a32-108">The first transform listed in **TRANSFORMS** must be an instance transform.</span></span> <span data-ttu-id="97a32-109">Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md)</span><span class="sxs-lookup"><span data-stu-id="97a32-109">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md)</span></span>

<span data-ttu-id="97a32-110">Essa propriedade está disponível com o instalador que executa um sistema no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="97a32-110">This property is available with the installer running a system in the Windows Server 2003 or Windows XP.</span></span>

## <a name="requirements"></a><span data-ttu-id="97a32-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97a32-111">Requirements</span></span>



| <span data-ttu-id="97a32-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="97a32-112">Requirement</span></span> | <span data-ttu-id="97a32-113">Valor</span><span class="sxs-lookup"><span data-stu-id="97a32-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a32-114">Versão</span><span class="sxs-lookup"><span data-stu-id="97a32-114">Version</span></span><br/> | <span data-ttu-id="97a32-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97a32-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="97a32-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="97a32-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="97a32-117">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="97a32-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="97a32-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="97a32-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97a32-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="97a32-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a32-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="97a32-120">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="97a32-121">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="97a32-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




