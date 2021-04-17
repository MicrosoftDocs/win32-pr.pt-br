---
description: Definir a propriedade TRANSFORMSSECURE como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Propriedade TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770174"
---
# <a name="transformssecure-property"></a><span data-ttu-id="84873-103">Propriedade TRANSFORMSSECURE</span><span class="sxs-lookup"><span data-stu-id="84873-103">TRANSFORMSSECURE property</span></span>

<span data-ttu-id="84873-104">Definir a propriedade **TRANSFORMSSECURE** como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="84873-104">Setting the **TRANSFORMSSECURE** property to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="84873-105">Definir essa propriedade é como definir a [política TransformsSecure](transformssecure-policy.md) , exceto que o escopo é diferente.</span><span class="sxs-lookup"><span data-stu-id="84873-105">Setting this property is like setting the [TransformsSecure policy](transformssecure-policy.md) except that the scope is different.</span></span> <span data-ttu-id="84873-106">A configuração da política TransformsSecure se aplica a todos os pacotes instalados por um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="84873-106">Setting TransformsSecure policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="84873-107">A definição da propriedade **TRANSFORMSSECURE** se aplica ao pacote, independentemente do usuário.</span><span class="sxs-lookup"><span data-stu-id="84873-107">Setting the **TRANSFORMSSECURE** property applies to the package regardless of the user.</span></span>

<span data-ttu-id="84873-108">A finalidade dessa propriedade é fornecer armazenamento de transformação seguro com usuários viajando do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="84873-108">The purpose of this property is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="84873-109">Quando essa propriedade é definida, uma [instalação de manutenção](maintenance-installation.md) só pode usar a transformação do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="84873-109">When this property is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the specified path.</span></span> <span data-ttu-id="84873-110">Se o caminho não estiver disponível, a instalação de manutenção falhará.</span><span class="sxs-lookup"><span data-stu-id="84873-110">If the path is not available the maintenance installation fails.</span></span> <span data-ttu-id="84873-111">Portanto, uma origem para cada transformação segura deve residir no local da origem do pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="84873-111">A source for each secure transform must therefore reside at the location of the source of the installation package.</span></span> <span data-ttu-id="84873-112">Em seguida, se o instalador descobrir que a transformação está ausente no computador local, ele poderá restaurar a transformação dessa fonte.</span><span class="sxs-lookup"><span data-stu-id="84873-112">Then if the installer finds that the transform is missing on the local computer, it can restore the transform from this source.</span></span>

## <a name="remarks"></a><span data-ttu-id="84873-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="84873-113">Remarks</span></span>

<span data-ttu-id="84873-114">Windows Installer interpreta a propriedade [**TRANSFORMSATSOURCE**](transformsatsource.md) como a mesma que a propriedade **TRANSFORMSSECURE** .</span><span class="sxs-lookup"><span data-stu-id="84873-114">Windows Installer interprets the [**TRANSFORMSATSOURCE**](transformsatsource.md) property to be the same as the **TRANSFORMSSECURE** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="84873-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84873-115">Requirements</span></span>



| <span data-ttu-id="84873-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="84873-116">Requirement</span></span> | <span data-ttu-id="84873-117">Valor</span><span class="sxs-lookup"><span data-stu-id="84873-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84873-118">Versão</span><span class="sxs-lookup"><span data-stu-id="84873-118">Version</span></span><br/> | <span data-ttu-id="84873-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="84873-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="84873-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="84873-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="84873-121">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="84873-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="84873-122">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="84873-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84873-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="84873-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84873-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="84873-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="84873-125">Transformações de banco de dados</span><span class="sxs-lookup"><span data-stu-id="84873-125">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




