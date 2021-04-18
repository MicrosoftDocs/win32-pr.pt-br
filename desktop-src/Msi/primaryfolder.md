---
description: O PRIMARYFOLDER é uma propriedade global que permite que o autor designe uma pasta principal para a instalação.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: Propriedade PRIMARYFOLDER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752031"
---
# <a name="primaryfolder-property"></a><span data-ttu-id="5de58-103">Propriedade PRIMARYFOLDER</span><span class="sxs-lookup"><span data-stu-id="5de58-103">PRIMARYFOLDER property</span></span>

<span data-ttu-id="5de58-104">O **PRIMARYFOLDER** é uma propriedade global que permite que o autor designe uma pasta principal para a instalação.</span><span class="sxs-lookup"><span data-stu-id="5de58-104">The **PRIMARYFOLDER** is a global property that allows the author to designate a primary folder for the installation.</span></span> <span data-ttu-id="5de58-105">O valor dessa propriedade deve ser o nome da chave de um diretório que existe na [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="5de58-105">The value for this property must be the key name of a directory that exists in the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="5de58-106">O instalador usa o caminho resolvido da pasta principal para determinar qual volume usar ao definir os valores da propriedade [**PrimaryVolumePath**](primaryvolumepath.md) , da propriedade [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , da propriedade [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) e da propriedade [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) .</span><span class="sxs-lookup"><span data-stu-id="5de58-106">The installer uses the resolved path of the primary folder to determine which volume to use when setting the values of the [**PrimaryVolumePath**](primaryvolumepath.md) property, [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) property, and [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) property.</span></span> <span data-ttu-id="5de58-107">O instalador fornece os valores dessas últimas Propriedades aos usuários na interface do usuário para ajudá-los a gerenciar o espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="5de58-107">The installer provides the values of these latter properties to users in the user interface to help them manage disk space.</span></span> <span data-ttu-id="5de58-108">Os autores de pacote normalmente podem selecionar a pasta maior que a pasta principal.</span><span class="sxs-lookup"><span data-stu-id="5de58-108">Commonly package authors can select the largest folder as the primary folder.</span></span>

<span data-ttu-id="5de58-109">O valor dessa propriedade deve ser o nome da chave de um registro de diretório encontrado na [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="5de58-109">The value for this property must be the key name of a directory record found in the [Directory table](directory-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5de58-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5de58-110">Requirements</span></span>



| <span data-ttu-id="5de58-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5de58-111">Requirement</span></span> | <span data-ttu-id="5de58-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5de58-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5de58-113">Versão</span><span class="sxs-lookup"><span data-stu-id="5de58-113">Version</span></span><br/> | <span data-ttu-id="5de58-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5de58-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5de58-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5de58-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5de58-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5de58-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5de58-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5de58-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5de58-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5de58-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de58-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5de58-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




