---
description: Gerenciador de Dispositivos Direct3D
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: Gerenciador de Dispositivos Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeff41b790df9537854ab715724d95cee646168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296150"
---
# <a name="direct3d-device-manager"></a><span data-ttu-id="a24c4-103">Gerenciador de Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="a24c4-103">Direct3D Device Manager</span></span>

<span data-ttu-id="a24c4-104">O Microsoft Direct3D Device Manager permite que dois ou mais objetos compartilhem o mesmo dispositivo Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a24c4-104">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span> <span data-ttu-id="a24c4-105">Um objeto atua como o proprietário do dispositivo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a24c4-105">One object acts as the owner of the Direct3D 9 device.</span></span> <span data-ttu-id="a24c4-106">Para compartilhar o dispositivo, o proprietário do dispositivo cria o Gerenciador de dispositivos do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a24c4-106">To share the device, the owner of the device creates the Direct3D device manager.</span></span> <span data-ttu-id="a24c4-107">Outros objetos podem obter um ponteiro para o Gerenciador de dispositivos do proprietário do dispositivo e, em seguida, usar o Gerenciador de dispositivos para obter um ponteiro para o dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a24c4-107">Other objects can obtain a pointer to the device manager from the device owner, then use the device manager to get a pointer to the Direct3D device.</span></span> <span data-ttu-id="a24c4-108">Qualquer objeto que usa o dispositivo mantém um bloqueio exclusivo, o que impede que outros objetos usem o dispositivo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a24c4-108">Any object that uses the device holds an exclusive lock, which prevents other objects from using the device at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="a24c4-109">O Direct3D Gerenciador de Dispositivos dá suporte apenas a dispositivos Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a24c4-109">The Direct3D Device Manager supports Direct3D 9 devices only.</span></span> <span data-ttu-id="a24c4-110">Ele não dá suporte a dispositivos DXGI.</span><span class="sxs-lookup"><span data-stu-id="a24c4-110">It does not support DXGI devices.</span></span>

 

<span data-ttu-id="a24c4-111">Para criar o Gerenciador de dispositivos do Direct3D, chame [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="a24c4-111">To create the Direct3D device manager, call [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span> <span data-ttu-id="a24c4-112">Essa função retorna um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) do Gerenciador de dispositivos, juntamente com um token de redefinição.</span><span class="sxs-lookup"><span data-stu-id="a24c4-112">This function returns a pointer to the device manager's [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface, along with a reset token.</span></span> <span data-ttu-id="a24c4-113">O token de redefinição permite que o proprietário do dispositivo Direct3D defina (e redefina) o dispositivo no Gerenciador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a24c4-113">The reset token enables the owner of the Direct3D device to set (and reset) the device on the device manager.</span></span> <span data-ttu-id="a24c4-114">Para inicializar o Gerenciador de dispositivos, chame [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="a24c4-114">To initialize the device manager, call [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span> <span data-ttu-id="a24c4-115">Passe um ponteiro para o dispositivo Direct3D, juntamente com o token de redefinição.</span><span class="sxs-lookup"><span data-stu-id="a24c4-115">Pass in a pointer to the Direct3D device, along with the reset token.</span></span>

<span data-ttu-id="a24c4-116">O código a seguir mostra como criar e inicializar o Gerenciador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a24c4-116">The following code shows how to create and initialize the device manager.</span></span>


```C++
HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&resetToken, &pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager->ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)->AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&pD3DManager);
    return hr;
}
```



<span data-ttu-id="a24c4-117">O proprietário do dispositivo deve fornecer uma maneira para que outros objetos obtenham um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="a24c4-117">The device owner must provide a way for other objects to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="a24c4-118">O mecanismo padrão é implementar a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="a24c4-118">The standard mechanism is to implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="a24c4-119">O GUID do serviço é \_ o \_ serviço de aceleração de vídeo Mr \_ .</span><span class="sxs-lookup"><span data-stu-id="a24c4-119">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="a24c4-120">Para compartilhar o dispositivo entre vários objetos, cada objeto (incluindo o proprietário do dispositivo) deve acessar o dispositivo por meio do Gerenciador de dispositivos, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a24c4-120">To share the device among several objects, each object (including the owner of the device) must access the device through the device manager, as follows:</span></span>

1.  <span data-ttu-id="a24c4-121">Chame [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obter um identificador para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a24c4-121">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the device.</span></span>
2.  <span data-ttu-id="a24c4-122">Para usar o dispositivo, chame [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) e passe o identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a24c4-122">To use the device, call [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) and pass in the device handle.</span></span> <span data-ttu-id="a24c4-123">O método retorna um ponteiro para a interface **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="a24c4-123">The method returns a pointer to the **IDirect3DDevice9** interface.</span></span> <span data-ttu-id="a24c4-124">O método pode ser chamado em um modo de bloqueio ou em um modo sem bloqueio, dependendo do valor do parâmetro *fBlock* .</span><span class="sxs-lookup"><span data-stu-id="a24c4-124">The method can be called in a blocking mode or a non-blocking mode, depending on the value of the *fBlock* parameter.</span></span>
3.  <span data-ttu-id="a24c4-125">Quando terminar de usar o dispositivo, chame [**IDirect3DDeviceManager9:: UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span><span class="sxs-lookup"><span data-stu-id="a24c4-125">When you are done using the device, call [**IDirect3DDeviceManager9::UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span></span> <span data-ttu-id="a24c4-126">Esse método torna o dispositivo disponível para outros objetos.</span><span class="sxs-lookup"><span data-stu-id="a24c4-126">This method makes the device available to other objects.</span></span>
4.  <span data-ttu-id="a24c4-127">Antes de sair, chame [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) para fechar o identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a24c4-127">Before exiting, call [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) to close the device handle.</span></span>

<span data-ttu-id="a24c4-128">Você deve manter o bloqueio do dispositivo somente durante o uso do dispositivo, pois manter o bloqueio do dispositivo impede que outros objetos usem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a24c4-128">You should hold the device lock only while using the device, because holding the device lock prevents other objects from using the device.</span></span>

<span data-ttu-id="a24c4-129">O proprietário do dispositivo pode alternar para outro dispositivo a qualquer momento chamando [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), normalmente porque o dispositivo original foi perdido.</span><span class="sxs-lookup"><span data-stu-id="a24c4-129">The owner of the device can switch to another device at any time by calling [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), typically because the original device was lost.</span></span> <span data-ttu-id="a24c4-130">A perda do dispositivo pode ocorrer por vários motivos, incluindo alterações na resolução do monitor, ações de gerenciamento de energia, bloqueio e desbloqueio do computador e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a24c4-130">Device loss can occur for various reasons, including changes in the monitor resolution, power management actions, locking and unlocking the computer, and so forth.</span></span> <span data-ttu-id="a24c4-131">Para obter mais informações, consulte a documentação do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a24c4-131">For more information, see the Direct3D documentation.</span></span>

<span data-ttu-id="a24c4-132">O método [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalida todos os identificadores de dispositivo que foram abertos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a24c4-132">The [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method invalidates any device handles that were opened previously.</span></span> <span data-ttu-id="a24c4-133">Quando um identificador de dispositivo é inválido, o método [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) retorna **DXVA2 \_ E \_ novo \_ \_ dispositivo de vídeo**.</span><span class="sxs-lookup"><span data-stu-id="a24c4-133">When a device handle is invalid, the [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method returns **DXVA2\_E\_NEW\_VIDEO\_DEVICE**.</span></span> <span data-ttu-id="a24c4-134">Se isso ocorrer, feche a alça e chame [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) novamente para obter um novo identificador de dispositivo, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a24c4-134">If this occurs, close the handle and call [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) again to obtain a new device handle, as shown in the following code.</span></span>

<span data-ttu-id="a24c4-135">O exemplo a seguir mostra como abrir um identificador de dispositivo e bloquear o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a24c4-135">The following example shows how to open a device handle and lock the device.</span></span>


```C++
HRESULT LockDevice(
    IDirect3DDeviceManager9 *pDeviceManager,
    BOOL fBlock,
    IDirect3DDevice9 **ppDevice, // Receives a pointer to the device.
    HANDLE *pHandle              // Receives a device handle.   
    )
{
    *pHandle = NULL;
    *ppDevice = NULL;

    HANDLE hDevice = 0;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);

    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->LockDevice(hDevice, ppDevice, fBlock);
    }

    if (hr == DXVA2_E_NEW_VIDEO_DEVICE)
    {
        // Invalid device handle. Try to open a new device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->OpenDeviceHandle(&hDevice);
        }

        // Try to lock the device again.
        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->LockDevice(hDevice, ppDevice, TRUE); 
        }
    }

    if (SUCCEEDED(hr))
    {
        *pHandle = hDevice;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a24c4-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a24c4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a24c4-137">Aceleração de vídeo do DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="a24c4-137">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



