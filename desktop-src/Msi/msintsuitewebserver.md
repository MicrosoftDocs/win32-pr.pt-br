---
description: No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteWebServer como 1 se o instalador estiver em execução em uma Web Edition do Windows Server 2003.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Propriedade MsiNTSuiteWebServer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787498"
---
# <a name="msintsuitewebserver-property"></a><span data-ttu-id="3e4f3-103">Propriedade MsiNTSuiteWebServer</span><span class="sxs-lookup"><span data-stu-id="3e4f3-103">MsiNTSuiteWebServer property</span></span>

<span data-ttu-id="3e4f3-104">No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteWebServer** como 1 se o instalador estiver em execução em uma Web Edition do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteWebServer** property to 1 if the installer is running on a web edition of the Windows Server 2003.</span></span> <span data-ttu-id="3e4f3-105">O instalador definirá essa propriedade como 1 somente se o \_ sinalizador de lâmina do pacote de ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="3e4f3-105">The installer sets this property to 1 only if the VER\_SUITE\_BLADE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="3e4f3-106">Caso contrário, o instalador não definirá essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-106">Otherwise the installer does not set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e4f3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e4f3-107">Remarks</span></span>

<span data-ttu-id="3e4f3-108">Essa propriedade só está disponível com a versão 2003 do Windows Server do instalador.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-108">This property is available only with the Windows Server 2003 release of the installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e4f3-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e4f3-109">Requirements</span></span>



| <span data-ttu-id="3e4f3-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e4f3-110">Requirement</span></span> | <span data-ttu-id="3e4f3-111">Valor</span><span class="sxs-lookup"><span data-stu-id="3e4f3-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4f3-112">Versão</span><span class="sxs-lookup"><span data-stu-id="3e4f3-112">Version</span></span><br/> | <span data-ttu-id="3e4f3-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3e4f3-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3e4f3-115">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3e4f3-116">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3e4f3-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e4f3-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e4f3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4f3-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e4f3-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="3e4f3-119">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="3e4f3-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
