---
description: A propriedade EXECUTEmode especifica como o instalador executa as atualizações do sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Propriedade EXECUTEmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758781"
---
# <a name="executemode-property"></a><span data-ttu-id="1b338-103">Propriedade EXECUTEmode</span><span class="sxs-lookup"><span data-stu-id="1b338-103">EXECUTEMODE property</span></span>

<span data-ttu-id="1b338-104">A propriedade **executemode** especifica como o instalador executa as atualizações do sistema.</span><span class="sxs-lookup"><span data-stu-id="1b338-104">The **EXECUTEMODE** property specifies how the installer executes system updates.</span></span> <span data-ttu-id="1b338-105">Essa propriedade pode ser útil quando for necessário executar uma instalação sem realmente alterar o sistema.</span><span class="sxs-lookup"><span data-stu-id="1b338-105">This property may be useful when it is necessary to run an installation without actually changing the system.</span></span> <span data-ttu-id="1b338-106">A propriedade pode ser definida como None para desabilitar as operações de atualização, como a instalação de arquivos e valores de registro.</span><span class="sxs-lookup"><span data-stu-id="1b338-106">The property can be set to None to disable updating operations such as the installation of files and registry values.</span></span>

<span data-ttu-id="1b338-107">Essa propriedade pode ter um dos dois valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b338-107">This property can have one of the following two values.</span></span> <span data-ttu-id="1b338-108">O instalador apenas examina a primeira letra do valor e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1b338-108">The installer only examines the first letter of the value and is case insensitive.</span></span>

<dl> <dt>

<span data-ttu-id="1b338-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span><span class="sxs-lookup"><span data-stu-id="1b338-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span>
</dt> <dd>

<span data-ttu-id="1b338-110">Nenhuma alteração é feita no sistema.</span><span class="sxs-lookup"><span data-stu-id="1b338-110">No changes are made to the system.</span></span> <span data-ttu-id="1b338-111">O instalador executa a interface do usuário e, em seguida, consulta o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1b338-111">The installer runs the user interface and then queries the database.</span></span>

</dd> <dt>

<span data-ttu-id="1b338-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Prescritiva</span><span class="sxs-lookup"><span data-stu-id="1b338-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script</span></span>
</dt> <dd>

<span data-ttu-id="1b338-113">Todas as alterações no sistema são feitas por meio de execução de script.</span><span class="sxs-lookup"><span data-stu-id="1b338-113">All changes to the system are made through script execution.</span></span> <span data-ttu-id="1b338-114">Esse é o modo padrão.</span><span class="sxs-lookup"><span data-stu-id="1b338-114">This is the default mode.</span></span>

</dd> </dl>

## <a name="default-value"></a><span data-ttu-id="1b338-115">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="1b338-115">Default Value</span></span>

<span data-ttu-id="1b338-116">Se essa propriedade não for definida, o modo de execução usa como padrão o script.</span><span class="sxs-lookup"><span data-stu-id="1b338-116">If this property is not defined, the execution mode defaults to Script.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b338-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b338-117">Requirements</span></span>



| <span data-ttu-id="1b338-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b338-118">Requirement</span></span> | <span data-ttu-id="1b338-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1b338-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b338-120">Versão</span><span class="sxs-lookup"><span data-stu-id="1b338-120">Version</span></span><br/> | <span data-ttu-id="1b338-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1b338-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1b338-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b338-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1b338-123">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1b338-123">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1b338-124">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1b338-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b338-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b338-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b338-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b338-126">Properties</span></span>](properties.md)
</dt> </dl>

 

 




