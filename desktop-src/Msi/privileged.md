---
description: A propriedade Privileged indica se a instalação é executada no contexto de privilégios elevados.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Propriedade privilegiada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748141"
---
# <a name="privileged-property"></a><span data-ttu-id="eed28-103">Propriedade privilegiada</span><span class="sxs-lookup"><span data-stu-id="eed28-103">Privileged property</span></span>

<span data-ttu-id="eed28-104">A propriedade **Privileged** indica se a instalação é executada no contexto de privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="eed28-104">The **Privileged** property indicates whether the installation is performed in the context of elevated privileges.</span></span> <span data-ttu-id="eed28-105">O instalador definirá essa propriedade se o usuário tiver privilégios de administrador, se o aplicativo tiver sido atribuído por um administrador de sistema ou se as políticas de usuário e máquina AlwaysInstallElevated estiverem definidas como true.</span><span class="sxs-lookup"><span data-stu-id="eed28-105">The installer sets this property if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="default-value"></a><span data-ttu-id="eed28-106">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="eed28-106">Default Value</span></span>

<span data-ttu-id="eed28-107">O instalador não definirá essa propriedade se o usuário não tiver permissão para instalar com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="eed28-107">The installer does not set this property if the user is not allowed to install with elevated privileges.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed28-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="eed28-108">Remarks</span></span>

<span data-ttu-id="eed28-109">Os desenvolvedores de pacotes do instalador podem usar a propriedade **Privileged** para tornar a instalação condicional na diretiva do sistema, o usuário sendo um administrador ou uma atribuição por um administrador.</span><span class="sxs-lookup"><span data-stu-id="eed28-109">Developers of installer packages can use the **Privileged** property to make the installation conditional upon system policy, the user being an administrator, or assignment by an administrator.</span></span>

<span data-ttu-id="eed28-110">Ao executar no Windows Vista, o **Privileged** e o [**AdminUser**](adminuser.md) são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="eed28-110">When running on Windows Vista, the **Privileged** and [**AdminUser**](adminuser.md) are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed28-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed28-111">Requirements</span></span>



| <span data-ttu-id="eed28-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed28-112">Requirement</span></span> | <span data-ttu-id="eed28-113">Valor</span><span class="sxs-lookup"><span data-stu-id="eed28-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed28-114">Versão</span><span class="sxs-lookup"><span data-stu-id="eed28-114">Version</span></span><br/> | <span data-ttu-id="eed28-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eed28-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eed28-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eed28-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eed28-117">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eed28-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="eed28-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="eed28-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eed28-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="eed28-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed28-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eed28-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




