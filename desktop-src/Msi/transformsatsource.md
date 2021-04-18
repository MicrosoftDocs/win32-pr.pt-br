---
description: Definir essa propriedade é como definir a política de política TransformsAtSource, exceto que o escopo é diferente.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Propriedade TRANSFORMSATSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785423"
---
# <a name="transformsatsource-property"></a><span data-ttu-id="7238a-103">Propriedade TRANSFORMSATSOURCE</span><span class="sxs-lookup"><span data-stu-id="7238a-103">TRANSFORMSATSOURCE property</span></span>

<span data-ttu-id="7238a-104">Definir essa propriedade é como definir a política de [política TransformsAtSource](transformsatsource-policy.md) , exceto que o escopo é diferente.</span><span class="sxs-lookup"><span data-stu-id="7238a-104">Setting this property is like setting the [TransformsAtSource policy](transformsatsource-policy.md) policy except that the scope is different.</span></span> <span data-ttu-id="7238a-105">A configuração da política TransformsAtSource se aplica a todos os pacotes instalados por um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="7238a-105">Setting TransformsAtSource policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="7238a-106">A definição da propriedade **TRANSFORMSATSOURCE** se aplica ao pacote, independentemente dos usuários.</span><span class="sxs-lookup"><span data-stu-id="7238a-106">Setting the **TRANSFORMSATSOURCE** property applies to the package regardless of the users.</span></span>

## <a name="remarks"></a><span data-ttu-id="7238a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7238a-107">Remarks</span></span>

<span data-ttu-id="7238a-108">Windows Installer interpreta a propriedade **TRANSFORMSATSOURCE** como se fosse a propriedade [**TRANSFORMSSECURE**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="7238a-108">Windows Installer interprets the **TRANSFORMSATSOURCE** property as though it were the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="7238a-109">Se o sinalizador @ for passado na propriedade [**TRANSformações**](transforms.md) , Windows Installer tratará as transformações na lista como [transformações de origem segura](secure-at-source-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="7238a-109">If the @ flag is passed in the [**TRANSFORMS**](transforms.md) property, Windows Installer treats the transforms in the list as [secure-at-source transforms](secure-at-source-transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7238a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7238a-110">Requirements</span></span>



| <span data-ttu-id="7238a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7238a-111">Requirement</span></span> | <span data-ttu-id="7238a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7238a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7238a-113">Versão</span><span class="sxs-lookup"><span data-stu-id="7238a-113">Version</span></span><br/> | <span data-ttu-id="7238a-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7238a-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7238a-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7238a-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7238a-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7238a-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7238a-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7238a-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7238a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7238a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7238a-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7238a-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




