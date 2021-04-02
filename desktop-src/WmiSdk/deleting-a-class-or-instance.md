---
description: Depois de terminar com uma classe ou uma instância, talvez você queira excluir essa classe ou instância do WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Excluindo uma classe ou instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165333"
---
# <a name="deleting-a-class-or-instance"></a><span data-ttu-id="4657d-103">Excluindo uma classe ou instância</span><span class="sxs-lookup"><span data-stu-id="4657d-103">Deleting a Class or Instance</span></span>

<span data-ttu-id="4657d-104">Depois de terminar com uma classe ou uma instância, talvez você queira excluir essa classe ou instância do WMI.</span><span class="sxs-lookup"><span data-stu-id="4657d-104">After you finish with a class or an instance, you may wish to delete that class or instance from WMI.</span></span> <span data-ttu-id="4657d-105">Assim como outras tecnologias orientadas a objeto, você pode excluir objetos de classe ou instância para limpar o namespace WMI e para retornar recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="4657d-105">Like other object-oriented technologies, you can delete class or instance objects to clean up the WMI namespace and to return system resources.</span></span> <span data-ttu-id="4657d-106">No entanto, muitas classes e instâncias no WMI são persistentes e são usadas por uma variedade de aplicativos a qualquer momento, portanto, você deve ter cuidado ao excluir uma classe ou instância WMI: seu aplicativo ou outro aplicativo provavelmente precisará da classe ou instância em uma data posterior.</span><span class="sxs-lookup"><span data-stu-id="4657d-106">However, many classes and instances in WMI are persistent and are used by a variety of applications at any given time Therefore, you should be careful when deleting a WMI class or instance: your application or another application will probably need the class or instance at a later date.</span></span>

<span data-ttu-id="4657d-107">Excluir uma classe ou uma instância é um procedimento simples.</span><span class="sxs-lookup"><span data-stu-id="4657d-107">Deleting a class or an instance is a simple procedure.</span></span> <span data-ttu-id="4657d-108">No entanto, devido à natureza permanente de uma classe, provavelmente não será necessário excluir uma classe com frequência.</span><span class="sxs-lookup"><span data-stu-id="4657d-108">However, due to the permanent nature of a class, you will probably not need to delete a class often.</span></span> <span data-ttu-id="4657d-109">Por exemplo, é improvável que você exclua a classe [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , pois é improvável que você não tenha uma unidade de disco em algum lugar em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="4657d-109">For example, you are unlikely to delete the [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) class, because it is unlikely that you do not have a disk drive somewhere in your enterprise.</span></span> <span data-ttu-id="4657d-110">Em vez disso, será mais provável que você exclua uma instância de uma classe.</span><span class="sxs-lookup"><span data-stu-id="4657d-110">Instead, you will be more likely to delete an instance of a class.</span></span> <span data-ttu-id="4657d-111">Para obter mais informações, consulte [excluindo uma instância](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="4657d-111">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span>

<span data-ttu-id="4657d-112">Embora não seja comum, você pode chegar a um momento em que deseja atualizar uma classe que você criou.</span><span class="sxs-lookup"><span data-stu-id="4657d-112">Although uncommon, you may come across a time where you wish to update a class that you created.</span></span> <span data-ttu-id="4657d-113">Por exemplo, você pode criar uma classe para representar um aplicativo de terceiros.</span><span class="sxs-lookup"><span data-stu-id="4657d-113">For example, you could create a class to represent a third-party application.</span></span> <span data-ttu-id="4657d-114">Se a terceira parte tiver atualizado seu software na medida em que sua classe não representou o software mais corretamente, talvez seja necessário excluir sua classe original.</span><span class="sxs-lookup"><span data-stu-id="4657d-114">If the third-party updated their software to the extent that your class no longer properly represented the software, you may need to delete your original class.</span></span> <span data-ttu-id="4657d-115">Para obter mais informações, consulte [excluindo uma classe](deleting-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="4657d-115">For more information, see [Deleting a Class](deleting-a-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4657d-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4657d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4657d-117">Criando classes formato MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="4657d-117">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
