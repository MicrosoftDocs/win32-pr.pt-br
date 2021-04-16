---
description: O instalador define o valor da Propriedade UserID como a representação da cadeia de caracteres do identificador de segurança (SID) do usuário que está executando a instalação. Para obter mais informações, consulte estruturas de autorização.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: Propriedade UserID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747314"
---
# <a name="usersid-property"></a><span data-ttu-id="581d2-104">Propriedade UserID</span><span class="sxs-lookup"><span data-stu-id="581d2-104">UserSID property</span></span>

<span data-ttu-id="581d2-105">O instalador define o valor da propriedade **userid** como a representação da cadeia de caracteres do identificador de segurança (SID) do usuário que está executando a instalação.</span><span class="sxs-lookup"><span data-stu-id="581d2-105">The installer sets the value of the **UserSID** property to the string representation of the security identifier (SID) of the user running the installation.</span></span> <span data-ttu-id="581d2-106">Para obter mais informações, consulte [estruturas de autorização](../secauthz/authorization-structures.md).</span><span class="sxs-lookup"><span data-stu-id="581d2-106">For more information, see [Authorization Structures](../secauthz/authorization-structures.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="581d2-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="581d2-107">Default Value</span></span>

<span data-ttu-id="581d2-108">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="581d2-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="581d2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="581d2-109">Remarks</span></span>

<span data-ttu-id="581d2-110">O Windows Installer definir essa propriedade no Windows 2000, Windows XP e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="581d2-110">The Windows Installer set this property on Windows 2000, Windows XP and Windows Vista.</span></span> <span data-ttu-id="581d2-111">Essa propriedade não está definida em todos os outros sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="581d2-111">This property is not defined on all other operating systems.</span></span>

<span data-ttu-id="581d2-112">Observe que essa propriedade tem o atributo especial que pode ser recuperado de uma ação personalizada adiada.</span><span class="sxs-lookup"><span data-stu-id="581d2-112">Note that this property has the special attribute that it can be retrieved from a deferred custom action.</span></span> <span data-ttu-id="581d2-113">Uma ação personalizada em execução com privilégios elevados ainda pode retornar o SID do usuário na propriedade **userid** .</span><span class="sxs-lookup"><span data-stu-id="581d2-113">A custom action running with elevated privileges can still return the user's SID in **UserSID** property.</span></span> <span data-ttu-id="581d2-114">Para obter informações, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="581d2-114">For information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="581d2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="581d2-115">Requirements</span></span>



| <span data-ttu-id="581d2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="581d2-116">Requirement</span></span> | <span data-ttu-id="581d2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="581d2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="581d2-118">Versão</span><span class="sxs-lookup"><span data-stu-id="581d2-118">Version</span></span><br/> | <span data-ttu-id="581d2-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="581d2-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="581d2-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="581d2-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="581d2-121">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="581d2-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="581d2-122">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="581d2-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="581d2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="581d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581d2-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="581d2-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 
