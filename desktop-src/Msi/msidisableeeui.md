---
description: Para desabilitar a interface do usuário inserida para a instalação definida na tabela MsiEmbeddedUI, defina a propriedade MSIDISABLEEEUI como 1 na linha de comando.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Propriedade MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757511"
---
# <a name="msidisableeeui-property"></a><span data-ttu-id="7000c-103">Propriedade MSIDISABLEEEUI</span><span class="sxs-lookup"><span data-stu-id="7000c-103">MSIDISABLEEEUI property</span></span>

<span data-ttu-id="7000c-104">Para desabilitar a interface do usuário inserida para a instalação definida na [tabela MsiEmbeddedUI](msiembeddedui-table.md), defina a propriedade MSIDISABLEEEUI como 1 na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="7000c-104">To disable the embedded user interface for the installation defined in the [MsiEmbeddedUI table](msiembeddedui-table.md), set the MSIDISABLEEEUI property to 1 on the command line.</span></span>

<span data-ttu-id="7000c-105">**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="7000c-105">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="7000c-106">Versões anteriores a Windows Installer 4,5 ignoram a propriedade MSIDISABLEEEUI.</span><span class="sxs-lookup"><span data-stu-id="7000c-106">Versions earlier than Windows Installer 4.5 ignore the MSIDISABLEEEUI Property.</span></span>

## <a name="remarks"></a><span data-ttu-id="7000c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7000c-107">Remarks</span></span>

<span data-ttu-id="7000c-108">Em uma instalação de vários pacotes, um pacote filho normalmente deve usar a interface do usuário do pacote pai e não inicializar sua própria interface de usuários inserida.</span><span class="sxs-lookup"><span data-stu-id="7000c-108">In a multiple-package installation, a child package should typically use the user interface of the parent package and not initialize its own embedded UI.</span></span> <span data-ttu-id="7000c-109">Se a propriedade MSIDISABLEEEUI não estiver definida dentro do pacote pai, o pacote filho usará a interface do usuário inserida do pacote pai por padrão e ignorará a propriedade MSIDISABLEEEUI dentro do pacote filho.</span><span class="sxs-lookup"><span data-stu-id="7000c-109">If the MSIDISABLEEEUI property is not set inside the parent package, the child package uses the embedded UI of the parent package by default and ignores the MSIDISABLEEEUI property within the child package.</span></span>

<span data-ttu-id="7000c-110">A propriedade MSIDISABLEEEUI desabilita a interface do usuário incorporada para um único pacote.</span><span class="sxs-lookup"><span data-stu-id="7000c-110">The MSIDISABLEEEUI property disables the embedded user interface for a single package.</span></span> <span data-ttu-id="7000c-111">Você pode usar a política [MsiDisableEmbeddedUI](msidisableembeddedui.md) para desabilitar interfaces de usuário inseridas para todos os pacotes no computador.</span><span class="sxs-lookup"><span data-stu-id="7000c-111">You can use the [MsiDisableEmbeddedUI](msidisableembeddedui.md) policy to disable embedded user interfaces for all packages on the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7000c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7000c-112">Requirements</span></span>



| <span data-ttu-id="7000c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7000c-113">Requirement</span></span> | <span data-ttu-id="7000c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7000c-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7000c-115">Versão</span><span class="sxs-lookup"><span data-stu-id="7000c-115">Version</span></span><br/> | <span data-ttu-id="7000c-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7000c-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7000c-117">Windows Installer 4,5 no Windows Server 2008, no Windows Vista, no Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7000c-117">Windows Installer 4.5 on Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="7000c-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7000c-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7000c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7000c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7000c-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7000c-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




