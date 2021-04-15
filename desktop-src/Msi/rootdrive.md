---
description: A propriedade ROOTDRIVE especifica a unidade padrão para o diretório de destino da instalação.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Propriedade ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760832"
---
# <a name="rootdrive-property"></a><span data-ttu-id="50c05-103">Propriedade ROOTDRIVE</span><span class="sxs-lookup"><span data-stu-id="50c05-103">ROOTDRIVE property</span></span>

<span data-ttu-id="50c05-104">A propriedade **ROOTDRIVE** especifica a unidade padrão para o diretório de destino da instalação.</span><span class="sxs-lookup"><span data-stu-id="50c05-104">The **ROOTDRIVE** property specifies the default drive for the destination directory of the installation.</span></span> <span data-ttu-id="50c05-105">Se a coluna Directory da [tabela de diretórios](directory-table.md) indicar o diretório de destino raiz por um nome de propriedade que está indefinido, o instalador usará o valor da propriedade **ROOTDRIVE** para resolver o caminho para o diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="50c05-105">If the Directory column of the [Directory table](directory-table.md) indicates the root destination directory by a property name that is undefined, the installer uses the value of the **ROOTDRIVE** property to resolve the path to the destination directory.</span></span>

<span data-ttu-id="50c05-106">Se **ROOTDRIVE** não estiver definido em uma linha de comando ou for criado na [tabela de propriedades](property-table.md), o instalador definirá essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="50c05-106">If **ROOTDRIVE** is not set at a command line or authored into the [Property table](property-table.md), the installer sets this property.</span></span> <span data-ttu-id="50c05-107">Durante uma [instalação administrativa](administrative-installation.md) , o instalador define **ROOTDRIVE** para a primeira unidade de rede conectada que pode ser gravada.</span><span class="sxs-lookup"><span data-stu-id="50c05-107">During an [administrative installation](administrative-installation.md) the installer sets **ROOTDRIVE** to the first connected network drive it finds that can be written to.</span></span> <span data-ttu-id="50c05-108">Se não for uma instalação administrativa ou se o instalador não encontrar unidades de rede, o instalador definirá **ROOTDRIVE** para a unidade local que pode ser gravada para ter mais espaço livre.</span><span class="sxs-lookup"><span data-stu-id="50c05-108">If it is not an administrative installation, or if the installer can find no network drives, the installer sets **ROOTDRIVE** to the local drive that can be written to having the most free space.</span></span>

<span data-ttu-id="50c05-109">O valor desta propriedade deve terminar com ' \\ '.</span><span class="sxs-lookup"><span data-stu-id="50c05-109">The value for this property must end with '\\'.</span></span>

## <a name="requirements"></a><span data-ttu-id="50c05-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50c05-110">Requirements</span></span>



| <span data-ttu-id="50c05-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="50c05-111">Requirement</span></span> | <span data-ttu-id="50c05-112">Valor</span><span class="sxs-lookup"><span data-stu-id="50c05-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c05-113">Versão</span><span class="sxs-lookup"><span data-stu-id="50c05-113">Version</span></span><br/> | <span data-ttu-id="50c05-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50c05-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="50c05-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="50c05-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="50c05-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="50c05-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="50c05-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="50c05-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50c05-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="50c05-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c05-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="50c05-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




