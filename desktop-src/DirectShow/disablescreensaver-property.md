---
description: A propriedade DVDAdm. DisableScreenSaver ativa ou desativa a proteção de tela do sistema.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Propriedade DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825525"
---
# <a name="disablescreensaver-property"></a><span data-ttu-id="a2e95-103">Propriedade DisableScreenSaver</span><span class="sxs-lookup"><span data-stu-id="a2e95-103">DisableScreenSaver Property</span></span>

> [!Note]  
> <span data-ttu-id="a2e95-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a2e95-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a2e95-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a2e95-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a2e95-106">A `DVDAdm.DisableScreenSaver` propriedade ativa ou desativa a proteção de tela do sistema.</span><span class="sxs-lookup"><span data-stu-id="a2e95-106">The `DVDAdm.DisableScreenSaver` property turns the system screen saver on or off.</span></span>

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a><span data-ttu-id="a2e95-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a2e95-107">Return Value</span></span>

<span data-ttu-id="a2e95-108">Retorna um valor booliano que indica se as configurações de proteção de tela do sistema estão desabilitadas para o aplicativo de DVD Player; verdadeiro significa que as configurações estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="a2e95-108">Returns a Boolean value indicating whether the system's screen saver settings are disabled for the DVD player application; true means the settings are disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2e95-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2e95-109">Remarks</span></span>

<span data-ttu-id="a2e95-110">Essa propriedade é de leitura/gravação com um valor padrão de true.</span><span class="sxs-lookup"><span data-stu-id="a2e95-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="a2e95-111">Ao exibir um disco DVD-Video, um usuário normalmente não usa o mouse ou o teclado por longos períodos de tempo.</span><span class="sxs-lookup"><span data-stu-id="a2e95-111">When viewing a DVD-Video disc, a user typically does not use the mouse or keyboard for extended periods of time.</span></span> <span data-ttu-id="a2e95-112">O MSWebDVD ActiveX® Control, portanto, desabilita a proteção de tela do sistema por padrão.</span><span class="sxs-lookup"><span data-stu-id="a2e95-112">The MSWebDVD ActiveX® control therefore disables the system screen saver by default.</span></span> <span data-ttu-id="a2e95-113">Objeto</span><span class="sxs-lookup"><span data-stu-id="a2e95-113">Object</span></span>

## <a name="see-also"></a><span data-ttu-id="a2e95-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2e95-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e95-115">**RestoreScreenSaver**</span><span class="sxs-lookup"><span data-stu-id="a2e95-115">**RestoreScreenSaver**</span></span>](restorescreensaver-method.md)
</dt> <dt>

[<span data-ttu-id="a2e95-116">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="a2e95-116">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



