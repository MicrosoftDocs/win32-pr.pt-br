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
# <a name="direct3d-device-manager"></a>Gerenciador de Dispositivos Direct3D

O Microsoft Direct3D Device Manager permite que dois ou mais objetos compartilhem o mesmo dispositivo Microsoft Direct3D 9. Um objeto atua como o proprietário do dispositivo Direct3D 9. Para compartilhar o dispositivo, o proprietário do dispositivo cria o Gerenciador de dispositivos do Direct3D. Outros objetos podem obter um ponteiro para o Gerenciador de dispositivos do proprietário do dispositivo e, em seguida, usar o Gerenciador de dispositivos para obter um ponteiro para o dispositivo Direct3D. Qualquer objeto que usa o dispositivo mantém um bloqueio exclusivo, o que impede que outros objetos usem o dispositivo ao mesmo tempo.

> [!Note]  
> O Direct3D Gerenciador de Dispositivos dá suporte apenas a dispositivos Direct3D 9. Ele não dá suporte a dispositivos DXGI.

 

Para criar o Gerenciador de dispositivos do Direct3D, chame [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9). Essa função retorna um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) do Gerenciador de dispositivos, juntamente com um token de redefinição. O token de redefinição permite que o proprietário do dispositivo Direct3D defina (e redefina) o dispositivo no Gerenciador de dispositivos. Para inicializar o Gerenciador de dispositivos, chame [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice). Passe um ponteiro para o dispositivo Direct3D, juntamente com o token de redefinição.

O código a seguir mostra como criar e inicializar o Gerenciador de dispositivos.


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



O proprietário do dispositivo deve fornecer uma maneira para que outros objetos obtenham um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . O mecanismo padrão é implementar a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . O GUID do serviço é \_ o \_ serviço de aceleração de vídeo Mr \_ .

Para compartilhar o dispositivo entre vários objetos, cada objeto (incluindo o proprietário do dispositivo) deve acessar o dispositivo por meio do Gerenciador de dispositivos, da seguinte maneira:

1.  Chame [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obter um identificador para o dispositivo.
2.  Para usar o dispositivo, chame [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) e passe o identificador do dispositivo. O método retorna um ponteiro para a interface **IDirect3DDevice9** . O método pode ser chamado em um modo de bloqueio ou em um modo sem bloqueio, dependendo do valor do parâmetro *fBlock* .
3.  Quando terminar de usar o dispositivo, chame [**IDirect3DDeviceManager9:: UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice). Esse método torna o dispositivo disponível para outros objetos.
4.  Antes de sair, chame [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) para fechar o identificador do dispositivo.

Você deve manter o bloqueio do dispositivo somente durante o uso do dispositivo, pois manter o bloqueio do dispositivo impede que outros objetos usem o dispositivo.

O proprietário do dispositivo pode alternar para outro dispositivo a qualquer momento chamando [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), normalmente porque o dispositivo original foi perdido. A perda do dispositivo pode ocorrer por vários motivos, incluindo alterações na resolução do monitor, ações de gerenciamento de energia, bloqueio e desbloqueio do computador e assim por diante. Para obter mais informações, consulte a documentação do Direct3D.

O método [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalida todos os identificadores de dispositivo que foram abertos anteriormente. Quando um identificador de dispositivo é inválido, o método [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) retorna **DXVA2 \_ E \_ novo \_ \_ dispositivo de vídeo**. Se isso ocorrer, feche a alça e chame [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) novamente para obter um novo identificador de dispositivo, conforme mostrado no código a seguir.

O exemplo a seguir mostra como abrir um identificador de dispositivo e bloquear o dispositivo.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



