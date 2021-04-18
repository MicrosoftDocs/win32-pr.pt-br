---
description: O instalador define a propriedade WindowsVolume para o volume da pasta do Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Propriedade WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750586"
---
# <a name="windowsvolume-property"></a><span data-ttu-id="2ee11-103">Propriedade WindowsVolume</span><span class="sxs-lookup"><span data-stu-id="2ee11-103">WindowsVolume property</span></span>

<span data-ttu-id="2ee11-104">O instalador define a propriedade **WindowsVolume** para o volume da pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="2ee11-104">The installer sets the **WindowsVolume** property to the volume of the windows folder.</span></span> <span data-ttu-id="2ee11-105">A propriedade sempre termina com uma barra invertida.</span><span class="sxs-lookup"><span data-stu-id="2ee11-105">The property always ends with a backslash.</span></span> <span data-ttu-id="2ee11-106">Isso pode ser usado para definir o local padrão para o volume em que a pasta do Windows está, porque a propriedade [**ROOTDRIVE**](rootdrive.md) não necessariamente é igual a essa unidade.</span><span class="sxs-lookup"><span data-stu-id="2ee11-106">This can be used to set the default location to the volume the Windows folder is on because the [**ROOTDRIVE**](rootdrive.md) property does not necessarily equal this drive.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ee11-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ee11-107">Remarks</span></span>

<span data-ttu-id="2ee11-108">Não use a propriedade **WindowsVolume** na coluna Directory da tabela [Directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee11-108">Do not use the **WindowsVolume** property in the Directory column of the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="2ee11-109">A propriedade [**WindowsFolder**](windowsfolder.md) contém o caminho para a pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="2ee11-109">The [**WindowsFolder**](windowsfolder.md) property contains the path to the Windows folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee11-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ee11-110">Requirements</span></span>



| <span data-ttu-id="2ee11-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ee11-111">Requirement</span></span> | <span data-ttu-id="2ee11-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2ee11-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee11-113">Versão</span><span class="sxs-lookup"><span data-stu-id="2ee11-113">Version</span></span><br/> | <span data-ttu-id="2ee11-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2ee11-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2ee11-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ee11-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2ee11-116">Windows Installer no Windows Server 2003 ou no Windows XP, consulte os [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2ee11-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ee11-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ee11-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee11-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ee11-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




