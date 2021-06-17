---
description: O instalador define a propriedade VersionNT64 como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriedade VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262068"
---
# <a name="versionnt64-property"></a><span data-ttu-id="1ae15-103">Propriedade VersionNT64</span><span class="sxs-lookup"><span data-stu-id="1ae15-103">VersionNT64 property</span></span>

<span data-ttu-id="1ae15-104">O instalador define a **propriedade VersionNT64** como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1ae15-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="1ae15-105">A propriedade será indefinida se o sistema operacional não for de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1ae15-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="1ae15-106">O valor é um inteiro: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="1ae15-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="1ae15-107">Por motivos de compatibilidade, a propriedade também [](template-summary.md) será indefinida se a propriedade Resumo do Modelo indicar que o pacote é para sistemas Intel (x86) de 32 bits e o sistema operacional não pode executar código Intel (x64) de 64 bits, como Windows 10 no ARM (ARM64).</span><span class="sxs-lookup"><span data-stu-id="1ae15-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel (x86) systems and the operating system cannot run 64-bit Intel (x64) code, such as Windows 10 on ARM (ARM64).</span></span>

> [!NOTE]
> <span data-ttu-id="1ae15-108">A partir Windows 10 Build 21277, os builds arm64 no canal de dev do programa Windows Insider Preview têm suporte para aplicativos x64.</span><span class="sxs-lookup"><span data-stu-id="1ae15-108">As of Windows 10 Build 21277, ARM64 builds in the Dev channel of the Windows Insider Preview program have support for x64 applications.</span></span> <span data-ttu-id="1ae15-109">Nesses builds arm64, a propriedade VersionNT64 é definida para pacotes x86.</span><span class="sxs-lookup"><span data-stu-id="1ae15-109">On these ARM64 builds, the VersionNT64 property is defined for x86 packages.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae15-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ae15-110">Remarks</span></span>

<span data-ttu-id="1ae15-111">As expressões condicionais testam o Windows de 64 bits simplesmente usando o nome da propriedade ou verificando a versão usando um operador de comparação.</span><span class="sxs-lookup"><span data-stu-id="1ae15-111">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae15-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ae15-112">Requirements</span></span>



| <span data-ttu-id="1ae15-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae15-113">Requirement</span></span> | <span data-ttu-id="1ae15-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1ae15-114">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae15-115">Versão</span><span class="sxs-lookup"><span data-stu-id="1ae15-115">Version</span></span><br/> | <span data-ttu-id="1ae15-116">Windows Installer 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1ae15-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1ae15-117">Windows Installer 4.0 ou Windows Installer 4.5 no Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ae15-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1ae15-118">Windows Installer windows server 2003 ou Windows XP Consulte os requisitos de [Windows Installer Run-Time](windows-installer-portal.md) para obter informações sobre o windows service pack mínimo exigido por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1ae15-118">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ae15-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ae15-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae15-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1ae15-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




