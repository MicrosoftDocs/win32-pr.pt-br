---
description: Eventos de extensão MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventos de extensão MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105816021"
---
# <a name="mtp-extension-events"></a><span data-ttu-id="52901-103">Eventos de extensão MTP</span><span class="sxs-lookup"><span data-stu-id="52901-103">MTP Extension Events</span></span>

<span data-ttu-id="52901-104">Os eventos notificam um aplicativo de que as alterações ocorreram em, ou com, um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="52901-104">Events notify an application that changes have occurred on, or with, a device.</span></span> <span data-ttu-id="52901-105">Por exemplo, um aplicativo pode se registrar para receber notificações de que um dispositivo foi removido.</span><span class="sxs-lookup"><span data-stu-id="52901-105">For example, an application can register to receive notfications that a device has been removed .</span></span>

## <a name="vendor-extended-event-codes"></a><span data-ttu-id="52901-106">Fornecedor-códigos de eventos estendidos</span><span class="sxs-lookup"><span data-stu-id="52901-106">Vendor-Extended Event Codes</span></span>

<span data-ttu-id="52901-107">Quando um fabricante de dispositivo dá suporte a um evento estendido pelo fornecedor, o driver combina o código de evento do fornecedor (UINT16) com os 16 bits mais altos do GUID de **\_ \_ \_ \_ \_ eventos estendidos do fornecedor do evento do WPD** .</span><span class="sxs-lookup"><span data-stu-id="52901-107">When a device manufacturer supports a vendor-extended event, their driver combines the vendor's event code (UINT16) with the highest 16 bits of the **WPD\_EVENT\_MTP\_VENDOR\_EXTENDED\_EVENTS** GUID.</span></span>

<span data-ttu-id="52901-108">Por exemplo, se o código estendido pelo fornecedor for 0xC001, o GUID resultante será como mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="52901-108">For example, if the vendor-extended code is 0xC001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a><span data-ttu-id="52901-109">Fornecedor-parâmetros de evento estendido</span><span class="sxs-lookup"><span data-stu-id="52901-109">Vendor-Extended Event Parameters</span></span>

<span data-ttu-id="52901-110">Os parâmetros para um evento estendido de fornecedor são relatados pelo GUID de eventos de **\_ parâmetro de evento \_ \_ \_ WPD** e pelos **\_ \_ \_ parâmetros de \_ evento \_ MTP ext de propriedade WPD**, que é uma coleção de **PROPVARIANTS**.</span><span class="sxs-lookup"><span data-stu-id="52901-110">The parameters for a vendor-extended event are reported by the **WPD\_EVENT\_PARAMETER\_EVENT\_ID** GUID and the **WPD\_PROPERTY\_MTP\_EXT\_EVENT\_PARAMS**, which is a collection of **PROPVARIANTS**.</span></span> <span data-ttu-id="52901-111">Esses **PROPVARIANTS** correspondem aos parâmetros do evento.</span><span class="sxs-lookup"><span data-stu-id="52901-111">These **PROPVARIANTS** correspond to the event parameters.</span></span> <span data-ttu-id="52901-112">Se não houver parâmetros, essa coleção estará vazia.</span><span class="sxs-lookup"><span data-stu-id="52901-112">If there are no parameters, this collection is empty.</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a><span data-ttu-id="52901-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52901-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52901-114">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="52901-114">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



