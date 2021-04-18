---
description: Os tópicos nesta seção fornecem as especificações de referência para as estruturas de pilha de entrada do dispositivo ponteiro.
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: Estruturas (entrada de dispositivo de ponteiro)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 988a66a65581cf97406ace5481f115b15a29329a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105790654"
---
# <a name="pointer-device-input-stack-structures"></a><span data-ttu-id="cf97c-103">Estruturas de pilha de entrada do dispositivo ponteiro</span><span class="sxs-lookup"><span data-stu-id="cf97c-103">Pointer Device Input Stack structures</span></span>

<span data-ttu-id="cf97c-104">Os tópicos nesta seção fornecem as especificações de referência para as estruturas de [pilha de entrada do dispositivo ponteiro](pointer-device-stack-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cf97c-104">The topics in this section provide the reference specifications for [Pointer Device Input Stack](pointer-device-stack-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cf97c-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="cf97c-105">In this section</span></span>

| <span data-ttu-id="cf97c-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="cf97c-106">Topic</span></span> | <span data-ttu-id="cf97c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf97c-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="cf97c-108">**POINTER_DEVICE_CURSOR_INFO**</span><span class="sxs-lookup"><span data-stu-id="cf97c-108">**POINTER_DEVICE_CURSOR_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | <span data-ttu-id="cf97c-109">Contém mapeamentos de ID de cursor para dispositivos de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="cf97c-109">Contains cursor ID mappings for pointer devices.</span></span><br/> |
| [<span data-ttu-id="cf97c-110">**POINTER_DEVICE_INFO**</span><span class="sxs-lookup"><span data-stu-id="cf97c-110">**POINTER_DEVICE_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | <span data-ttu-id="cf97c-111">Contém informações sobre um dispositivo de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="cf97c-111">Contains information about a pointer device.</span></span> <span data-ttu-id="cf97c-112">Uma matriz dessas estruturas é retornada da função [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) .</span><span class="sxs-lookup"><span data-stu-id="cf97c-112">An array of these structures is returned from the [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) function.</span></span> <span data-ttu-id="cf97c-113">Uma única estrutura é retornada de uma chamada para a função [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) .</span><span class="sxs-lookup"><span data-stu-id="cf97c-113">A single structure is returned from a call to the [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) function.</span></span> <br/> |
| [<span data-ttu-id="cf97c-114">**POINTER_DEVICE_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="cf97c-114">**POINTER_DEVICE_PROPERTY**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | <span data-ttu-id="cf97c-115">Contém as propriedades do dispositivo (dispositivos de interface humana (HID) itens globais que correspondem aos usos de HID).</span><span class="sxs-lookup"><span data-stu-id="cf97c-115">Contains device properties (Human Interface Device (HID) global items that correspond to HID usages).</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="cf97c-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf97c-116">Related topics</span></span>

[<span data-ttu-id="cf97c-117">Referência de pilha de entrada do dispositivo ponteiro</span><span class="sxs-lookup"><span data-stu-id="cf97c-117">Pointer Device Input Stack Reference</span></span>](unified-input-stack-reference.md)
