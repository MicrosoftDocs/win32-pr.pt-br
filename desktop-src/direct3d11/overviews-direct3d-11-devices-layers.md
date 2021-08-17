---
title: Camadas de software
description: O runtime do Direct3D 11 é construído com camadas, começando com a funcionalidade básica no núcleo e criando funcionalidades opcionais e de assistência do desenvolvedor em camadas externas. Esta seção descreve a funcionalidade de cada camada.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59d0405d53526b8fb0b93e52fd1a53b5c17839f6c58df919bac335b21ad2477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124356"
---
# <a name="software-layers"></a>Camadas de software

O runtime do Direct3D 11 é construído com camadas, começando com a funcionalidade básica no núcleo e criando funcionalidades opcionais e de assistência do desenvolvedor em camadas externas. Esta seção descreve a funcionalidade de cada camada.

Como regra geral, as camadas adicionam funcionalidade, mas não modificam o comportamento existente. Por exemplo, as funções principais terão os mesmos valores de retorno independentes da camada de depuração que está sendo instautada, embora a saída de depuração adicional possa ser fornecida se a camada de depuração for instautada.

Para criar camadas quando um dispositivo é criado, chame [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e fornece um ou mais valores de SINALIZADOR DE DISPOSITIVO [**DE CRIAÇÃO D3D11. \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)

O Direct3D 11 fornece as seguintes camadas de runtime:

-   [Camada principal](#core-layer)
-   [Camada de depuração](#debug-layer)
-   [Tópicos relacionados](#related-topics)

## <a name="core-layer"></a>Camada principal

A camada principal existe por padrão; fornecendo um mapeamento muito fino entre a API e o driver de dispositivo, minimizando a sobrecarga para chamadas de alta frequência. Como a camada principal é essencial para o desempenho, ela só executa a validação crítica. As camadas restantes são opcionais.

## <a name="debug-layer"></a>Camada de depuração

A camada de depuração fornece uma ampla validação de consistência e parâmetro adicional (como validar vinculação de sombreador e associação de recursos, validar a consistência do parâmetro e relatar descrições de erro).

Para criar um dispositivo que dá suporte à camada de depuração, você deve instalar o SDK do DirectX (para obter D3D11SDKLayers.dll) e especificar o sinalizador **D3D11 \_ CREATE \_ DEVICE \_ DEBUG** ao chamar a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou a função [**D3D11CreateDeviceAndSwapChain.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) Se você executar seu aplicativo com a camada de depuração habilitada, o aplicativo será substancialmente mais lento. Mas, para garantir que seu aplicativo seja limpo de erros e avisos antes de você o enviar, use a camada de depuração. Para obter mais informações, consulte [Usando a camada de depuração para depurar aplicativos](using-the-debug-layer-to-test-apps.md).


> [!Note]  
> Para o Windows 7 com a Atualização de Plataforma para Windows 7 (KB2670838) ou Windows 8.x, para criar um dispositivo que dá suporte à camada de depuração, instale o SDK (Software Development Kit) do Windows para Windows 8.x para obter o D3D11 \_1SDKLayers.dll.


> [!Note]  
> Por Windows 10, para criar um dispositivo que dá suporte à camada de depuração, habilita o recurso opcional "Ferramentas gráficas". Acesse o painel Configurações, em Sistema, Aplicativos & recursos, Gerenciar recursos opcionais, Adicionar um recurso e, em seguida, procure "Ferramentas gráficas".


> [!Note]  
> Para obter informações sobre como depurar aplicativos DirectX remotamente, consulte [Depurando aplicativos DirectX remotamente.](/windows/desktop/direct3dtools/debugging-directx-apps-remotely)

 

Como alternativa, você pode habilitar/desabilitar o sinalizador de depuração usando o [Painel de Controle DirectX](/previous-versions//bb219725(v=vs.85)) incluído como parte do SDK do DirectX.

Quando a camada de depuração lista vazamentos de memória, ela emita uma lista de ponteiros de interface de objeto juntamente com seus nomes amigáveis. O nome amigável padrão é " &lt; sem nome &gt; ". Você pode definir o nome amigável usando o método [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) e o GUID **WKPDID \_ D3DDebugObjectName** que está em D3Dcommon.h. Por exemplo, para nomear pTexture com um nome SDKLayer de mytexture.jpg, use o seguinte código:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



Normalmente, você deve compilar essas chamadas da versão de produção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 