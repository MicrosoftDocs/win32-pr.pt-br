---
description: O método DVDAdm. RestoreScreenSaver restaura as configurações de proteção de tela do sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Método RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754212"
---
# <a name="restorescreensaver-method"></a><span data-ttu-id="f8c78-103">Método RestoreScreenSaver</span><span class="sxs-lookup"><span data-stu-id="f8c78-103">RestoreScreenSaver Method</span></span>

> [!Note]  
> <span data-ttu-id="f8c78-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f8c78-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f8c78-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f8c78-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f8c78-106">O `DVDAdm.RestoreScreenSaver` método restaura as configurações de proteção de tela do sistema.</span><span class="sxs-lookup"><span data-stu-id="f8c78-106">The `DVDAdm.RestoreScreenSaver` method restores the system screen saver settings.</span></span>

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a><span data-ttu-id="f8c78-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f8c78-107">Return Value</span></span>

<span data-ttu-id="f8c78-108">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f8c78-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c78-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8c78-109">Remarks</span></span>

<span data-ttu-id="f8c78-110">Em geral, um aplicativo de DVD desabilitará a proteção de tela do sistema na inicialização definindo a propriedade [**DisableScreenSaver**](disablescreensaver-property.md) como true e, em seguida, reabilitará novamente a proteção de tela quando o aplicativo de DVD for fechado chamando `RestoreScreenSaver` .</span><span class="sxs-lookup"><span data-stu-id="f8c78-110">Generally, a DVD application will disable the system's screen saver on startup by setting the [**DisableScreenSaver**](disablescreensaver-property.md) property to true, and then re-enable the screen saver again when the DVD application is closed by calling `RestoreScreenSaver`.</span></span> <span data-ttu-id="f8c78-111">Se um aplicativo não usar as configurações de proteção de tela do sistema, ele não precisará chamar esse método ou definir a propriedade **DisableScreenSaver** .</span><span class="sxs-lookup"><span data-stu-id="f8c78-111">If an application does not use the system's screen saver settings, it does not have to call this method or set the **DisableScreenSaver** property.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8c78-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8c78-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c78-113">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="f8c78-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



