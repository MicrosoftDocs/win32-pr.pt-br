---
description: A propriedade TARGETDIR especifica o diretório de destino raiz para a instalação.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: Propriedade TARGETDIR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759371"
---
# <a name="targetdir-property"></a><span data-ttu-id="ff02f-103">Propriedade TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="ff02f-103">TARGETDIR property</span></span>

<span data-ttu-id="ff02f-104">A propriedade **TARGETDIR** especifica o diretório de destino raiz para a instalação.</span><span class="sxs-lookup"><span data-stu-id="ff02f-104">The **TARGETDIR** property specifies the root destination directory for the installation.</span></span> <span data-ttu-id="ff02f-105">**TARGETDIR** deve ser o nome de uma raiz na tabela de [diretórios](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ff02f-105">**TARGETDIR** must be the name of one root in the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="ff02f-106">Pode haver apenas um único diretório de destino raiz.</span><span class="sxs-lookup"><span data-stu-id="ff02f-106">There may be only a single root destination directory.</span></span> <span data-ttu-id="ff02f-107">Durante uma [instalação administrativa](administrative-installation.md) , essa propriedade especifica o local para copiar o pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="ff02f-107">During an [administrative installation](administrative-installation.md) this property specifies the location to copy the installation package.</span></span> <span data-ttu-id="ff02f-108">Durante uma instalação não administrativa, essa propriedade especifica o diretório de destino raiz.</span><span class="sxs-lookup"><span data-stu-id="ff02f-108">During a non-administrative installation this property specifies the root destination directory.</span></span>

<span data-ttu-id="ff02f-109">Para especificar o diretório de destino raiz, defina a coluna Directory da tabela Directory como a propriedade **TARGETDIR** e a coluna DefaultDir como a propriedade [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="ff02f-109">To specify the root destination directory, set the Directory column of the Directory table to the **TARGETDIR** property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="ff02f-110">Se a propriedade **TARGETDIR** for definida, o diretório de destino será resolvido para o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ff02f-110">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="ff02f-111">Se a propriedade **TARGETDIR** for indefinida, a propriedade [**ROOTDRIVE**](rootdrive.md) será usada para resolver o caminho.</span><span class="sxs-lookup"><span data-stu-id="ff02f-111">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span> <span data-ttu-id="ff02f-112">Para obter mais informações sobre como usar a propriedade **TARGETDIR** , consulte [usando a tabela de diretórios](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff02f-112">For more information about using the **TARGETDIR** property, see [Using the Directory Table](using-the-directory-table.md).</span></span>

<span data-ttu-id="ff02f-113">Observe que o valor da propriedade **TARGETDIR** normalmente é definido na linha de comando ou por meio de uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff02f-113">Note that the value of the **TARGETDIR** property is typically set at the command line or through a user interface.</span></span> <span data-ttu-id="ff02f-114">A definição de **TARGETDIR** por meio da criação de um caminho na [tabela de propriedades](property-table.md) não é recomendada porque os computadores diferem na configuração da unidade local.</span><span class="sxs-lookup"><span data-stu-id="ff02f-114">Setting **TARGETDIR** by authoring a path into the [Property table](property-table.md) is not recommended because computers differ in the set up of the local drive.</span></span>

<span data-ttu-id="ff02f-115">Para obter mais informações sobre como alterar TARGETDIR durante uma instalação, consulte [alterando o local de destino de um diretório](changing-the-target-location-for-a-directory.md)</span><span class="sxs-lookup"><span data-stu-id="ff02f-115">For more information on how to change TARGETDIR during an installation see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="ff02f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff02f-116">Requirements</span></span>



| <span data-ttu-id="ff02f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff02f-117">Requirement</span></span> | <span data-ttu-id="ff02f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ff02f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff02f-119">Versão</span><span class="sxs-lookup"><span data-stu-id="ff02f-119">Version</span></span><br/> | <span data-ttu-id="ff02f-120">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ff02f-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ff02f-121">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ff02f-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ff02f-122">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff02f-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ff02f-123">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ff02f-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff02f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff02f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff02f-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ff02f-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




