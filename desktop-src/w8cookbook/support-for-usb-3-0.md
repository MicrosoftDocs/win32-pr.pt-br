---
title: Suporte para USB 3,0
description: Suporte para USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103641964"
---
# <a name="support-for-usb-30"></a><span data-ttu-id="d3e04-103">Suporte para USB 3,0</span><span class="sxs-lookup"><span data-stu-id="d3e04-103">Support for USB 3.0</span></span>

## <a name="platforms"></a><span data-ttu-id="d3e04-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="d3e04-104">Platforms</span></span>

<span data-ttu-id="d3e04-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="d3e04-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="d3e04-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3e04-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="d3e04-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3e04-107">Description</span></span>

<span data-ttu-id="d3e04-108">No Windows 8 e no Windows Server 2012, adicionamos suporte para USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="d3e04-108">In Windows 8 and Windows Server 2012, we added support for USB 3.0.</span></span> <span data-ttu-id="d3e04-109">Fizemos isso adicionando uma nova pilha de software para ligar o controlador de host USB 3,0, chamado de XHC (controlador de host extensível).</span><span class="sxs-lookup"><span data-stu-id="d3e04-109">We did this by adding a new software stack to power the USB 3.0 host controller, called an eXtensible Host Controller (XHC).</span></span> <span data-ttu-id="d3e04-110">Mantivemos a paridade da interface, o nível de IRQL, o contexto do chamador, o status do erro, a frequência de repetição e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d3e04-110">We maintained interface parity, IRQL level, caller context, error status, retry frequency, and so on.</span></span> <span data-ttu-id="d3e04-111">Não deve haver nenhuma diferença para você ao interagir com um dispositivo conectado por USB 2,0 versus USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="d3e04-111">There should be no difference for you when interacting with a device connected over USB 2.0 versus USB 3.0.</span></span>

<span data-ttu-id="d3e04-112">No entanto, se você estiver escrevendo um driver para um novo dispositivo USB 3,0, definitivamente, opte por novos recursos de USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="d3e04-112">However, if you are writing a driver for a new, USB 3.0 device, definitely opt for new USB 3.0 capabilities.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d3e04-113">Manifestação</span><span class="sxs-lookup"><span data-stu-id="d3e04-113">Manifestation</span></span>

<span data-ttu-id="d3e04-114">As transferências de dispositivo são mais rápidas e menos energia são consumidas de um PC por dispositivos USB em geral.</span><span class="sxs-lookup"><span data-stu-id="d3e04-114">Device transfers are faster and less power is consumed from a PC by USB devices overall.</span></span> <span data-ttu-id="d3e04-115">Há um risco de que os dispositivos USB existentes não funcionem corretamente quando conectados a uma porta USB 3,0.</span><span class="sxs-lookup"><span data-stu-id="d3e04-115">There is a risk that existing USB devices may not function correctly when connected to a USB 3.0 port.</span></span> <span data-ttu-id="d3e04-116">Isso não deve acontecer e não é esperado, mas, como o software que alimenta o USB 3,0 é novo, é um risco.</span><span class="sxs-lookup"><span data-stu-id="d3e04-116">This should not happen, and is not expected, but, because the software that powers USB 3.0 is new, it is a risk.</span></span>

 

 




