---
title: Tratamento de erros e remoção de dispositivo no DirectML
description: Este tópico discute como depurar DirectML dispositivos-remoção e outras condições de erro.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548252"
---
# <a name="handling-errors-and-device-removal-in-directml"></a><span data-ttu-id="c2d90-103">Tratamento de erros e remoção de dispositivo no DirectML</span><span class="sxs-lookup"><span data-stu-id="c2d90-103">Handling errors and device-removal in DirectML</span></span>

## <a name="device-removal"></a><span data-ttu-id="c2d90-104">Dispositivo-remoção</span><span class="sxs-lookup"><span data-stu-id="c2d90-104">Device-removal</span></span>

<span data-ttu-id="c2d90-105">Se ocorrer um erro irrecuperável, o dispositivo DirectML poderá inserir um estado de "dispositivo removido".</span><span class="sxs-lookup"><span data-stu-id="c2d90-105">If an unrecoverable error occurs, the DirectML device may enter a "device-removed" state.</span></span> <span data-ttu-id="c2d90-106">Erros irrecuperáveis que causam a remoção de dispositivo incluem uso de API inválido (para métodos que não retornam um [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), erro de driver, falha de hardware ou condições de OOM (memória insuficiente).</span><span class="sxs-lookup"><span data-stu-id="c2d90-106">Unrecoverable errors that cause device-removal include invalid API usage (for methods that don't return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), driver error, hardware fault, or out-of-memory (OOM) conditions.</span></span>

<span data-ttu-id="c2d90-107">Quando um dispositivo DirectML é removido, todas as chamadas de método no dispositivo e todos os objetos criados por esse dispositivo tornam-se sem operações.</span><span class="sxs-lookup"><span data-stu-id="c2d90-107">When a DirectML device is removed, all method calls on the device, and every object created by that device, become no-ops.</span></span> <span data-ttu-id="c2d90-108">Para métodos que retornam um [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), um código de erro [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) é retornado.</span><span class="sxs-lookup"><span data-stu-id="c2d90-108">For methods that return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), a [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) error code is returned.</span></span> <span data-ttu-id="c2d90-109">Você pode usar o [método **IDMLDevice:: GetDeviceRemovedReason**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) para verificar se o dispositivo DirectML foi removido e para recuperar um código de erro mais detalhado.</span><span class="sxs-lookup"><span data-stu-id="c2d90-109">You can use the [**IDMLDevice::GetDeviceRemovedReason** method](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) to check whether the DirectML device has been removed, and to retrieve a more detailed error code.</span></span>

<span data-ttu-id="c2d90-110">Não é possível recuperar-se da remoção do dispositivo, exceto liberando o dispositivo afetado e todos os seus filhos e recriando o dispositivo DirectML do zero.</span><span class="sxs-lookup"><span data-stu-id="c2d90-110">You can't recover from device-removal except by releasing the affected device and all its children, then re-creating the DirectML device from scratch.</span></span>

<span data-ttu-id="c2d90-111">O dispositivo-remoção do dispositivo Direct3D 12 subjacente também faz com que o dispositivo DirectML seja removido.</span><span class="sxs-lookup"><span data-stu-id="c2d90-111">Device-removal of the underlying Direct3D 12 device also causes the DirectML device to be removed.</span></span> <span data-ttu-id="c2d90-112">No entanto, o inverso não é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="c2d90-112">However, the reverse is not true.</span></span> <span data-ttu-id="c2d90-113">Dispositivo DirectML-a remoção pode não fazer necessariamente com que o dispositivo Direct3D 12 subjacente seja removido.</span><span class="sxs-lookup"><span data-stu-id="c2d90-113">DirectML device-removal may not necessarily cause the underlying Direct3D 12 device to become removed.</span></span>

## <a name="debugging-directml-device-removal-and-other-errors"></a><span data-ttu-id="c2d90-114">Depuração do dispositivo DirectML-remoção e outros erros</span><span class="sxs-lookup"><span data-stu-id="c2d90-114">Debugging DirectML device-removal, and other errors</span></span>

<span data-ttu-id="c2d90-115">A causa mais comum de erros de DirectML é o uso inválido da API.</span><span class="sxs-lookup"><span data-stu-id="c2d90-115">The most common cause of DirectML errors is invalid API usage.</span></span> <span data-ttu-id="c2d90-116">O uso inválido da API pode resultar em um **E_INVALIDARG** código de erro HRESULT ou pode resultar na remoção do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2d90-116">Invalid API usage might result in an **E_INVALIDARG** HRESULT error code, or it might result in device-removal.</span></span>

<span data-ttu-id="c2d90-117">É altamente recomendável que você habilite a [camada de depuração DirectML](dml-debug-layer.md) durante seu desenvolvimento, para detectar e depurar esses erros.</span><span class="sxs-lookup"><span data-stu-id="c2d90-117">We strongly recommend that you enable the [DirectML debug layer](dml-debug-layer.md) during your development, in order to catch and debug such errors.</span></span> <span data-ttu-id="c2d90-118">A camada de depuração DirectML executa uma extensa validação dos parâmetros do método e do uso da API e emitirá mensagens de saída de depuração para ajudá-lo a depurar.</span><span class="sxs-lookup"><span data-stu-id="c2d90-118">The DirectML debug layer performs extensive validation of method parameters and API usage, and it will emit debug output messages to help you debug.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2d90-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2d90-119">See also</span></span>

* [<span data-ttu-id="c2d90-120">Usando a camada de depuração DirectML</span><span class="sxs-lookup"><span data-stu-id="c2d90-120">Using the DirectML debug layer</span></span>](dml-debug-layer.md)
