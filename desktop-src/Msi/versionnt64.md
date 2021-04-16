---
description: O instalador definirá a propriedade VersionNT64 como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriedade VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757777"
---
# <a name="versionnt64-property"></a><span data-ttu-id="6b520-103">Propriedade VersionNT64</span><span class="sxs-lookup"><span data-stu-id="6b520-103">VersionNT64 property</span></span>

<span data-ttu-id="6b520-104">O instalador definirá a propriedade **VersionNT64** como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6b520-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="6b520-105">A propriedade será indefinida se o sistema operacional não for de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6b520-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="6b520-106">O valor é um inteiro: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="6b520-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="6b520-107">Por motivos de compatibilidade, a propriedade também será indefinida se a propriedade de [**Resumo do modelo**](template-summary.md) indicar que o pacote é para sistemas Intel de 32 bits e o sistema operacional é uma arquitetura de 64 bits que não é Intel64 ou x64 (como ARM64).</span><span class="sxs-lookup"><span data-stu-id="6b520-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel systems and the operating system is a 64-bit architecture that is not Intel64 or x64 (such as ARM64).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b520-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b520-108">Remarks</span></span>

<span data-ttu-id="6b520-109">As expressões condicionais testam as janelas de 64 bits simplesmente usando o nome da propriedade ou verificando a versão usando um operador de comparação.</span><span class="sxs-lookup"><span data-stu-id="6b520-109">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b520-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b520-110">Requirements</span></span>



| <span data-ttu-id="6b520-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b520-111">Requirement</span></span> | <span data-ttu-id="6b520-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6b520-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b520-113">Versão</span><span class="sxs-lookup"><span data-stu-id="6b520-113">Version</span></span><br/> | <span data-ttu-id="6b520-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6b520-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6b520-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6b520-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6b520-116">Windows Installer no Windows Server 2003 ou no Windows XP, consulte os [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6b520-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b520-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b520-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b520-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6b520-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




