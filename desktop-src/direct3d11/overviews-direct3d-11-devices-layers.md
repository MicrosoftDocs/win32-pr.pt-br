---
title: Camadas de software
description: O tempo de execução do Direct3D 11 é construído com camadas, começando com a funcionalidade básica no núcleo e criando a funcionalidade opcional e auxiliar de desenvolvedor em camadas externas. Esta seção descreve a funcionalidade de cada camada.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499050"
---
# <a name="software-layers"></a>Camadas de software

O tempo de execução do Direct3D 11 é construído com camadas, começando com a funcionalidade básica no núcleo e criando a funcionalidade opcional e auxiliar de desenvolvedor em camadas externas. Esta seção descreve a funcionalidade de cada camada.

Como regra geral, as camadas adicionam funcionalidade, mas não modificam o comportamento existente. Por exemplo, as funções principais terão os mesmos valores de retorno independentes da camada de depuração que está sendo instanciada, embora a saída de depuração adicional possa ser fornecida se a camada de depuração for instanciada.

Para criar camadas quando um dispositivo é criado, chame [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e forneça um ou mais valores de [**\_ sinalizador de \_ dispositivo \_ D3D11 criar**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .

O Direct3D 11 fornece as seguintes camadas de tempo de execução:

-   [Camada principal](#core-layer)
-   [Camada de depuração](#debug-layer)
-   [Tópicos relacionados](#related-topics)

## <a name="core-layer"></a>Camada principal

A camada principal existe por padrão; fornecendo um mapeamento muito fino entre a API e o driver de dispositivo, minimizando a sobrecarga para chamadas de alta frequência. Como a camada principal é essencial para o desempenho, ela executa apenas a validação crítica. As camadas restantes são opcionais.

## <a name="debug-layer"></a>Camada de depuração

A camada de depuração fornece um parâmetro adicional e validação de consistência (como validação de vínculo de sombreador e vinculação de recursos, validação de consistência de parâmetro e descrições de erro de relatório).

Para criar um dispositivo que dê suporte à camada de depuração, você deve instalar o SDK do DirectX (para obter D3D11SDKLayers.dll) e, em seguida, especificar o sinalizador de **\_ \_ \_ depuração do dispositivo D3D11 Create** ao chamar a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou a função [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) . Se você executar o aplicativo com a camada de depuração habilitada, o aplicativo será consideravelmente mais lento. Mas, para garantir que seu aplicativo esteja sem erros e avisos antes de enviá-lo, use a camada de depuração. Para obter mais informações, consulte [usando a camada de depuração para depurar aplicativos](using-the-debug-layer-to-test-apps.md).


> [!Note]  
> Para o Windows 7 com a atualização de plataforma para Windows 7 (KB2670838) ou Windows 8. x, para criar um dispositivo que dê suporte à camada de depuração, instale o SDK (Software Development Kit) do Windows para Windows 8. x para obter o D3D11 \_1SDKLayers.dll.


> [!Note]  
> Para o Windows 10, para criar um dispositivo que dê suporte à camada de depuração, habilite o recurso opcional "ferramentas de gráficos". Vá para o painel configurações, em sistema, aplicativos & recursos, gerencie recursos opcionais, adicione um recurso e procure "ferramentas de gráficos".


> [!Note]  
> Para obter informações sobre como depurar aplicativos DirectX remotamente, consulte [Depurando aplicativos DirectX remotamente](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).

 

Como alternativa, você pode habilitar/desabilitar o sinalizador de depuração usando o [painel de controle do DirectX](/previous-versions//bb219725(v=vs.85)) incluído como parte do SDK do DirectX.

Quando a camada de depuração lista vazamentos de memória, ela gera uma lista de ponteiros de interface de objeto junto com seus nomes amigáveis. O nome amigável padrão é " &lt; sem nome &gt; ". Você pode definir o nome amigável usando o método [**ID3D11DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) e o GUID **WKPDID \_ D3DDebugObjectName** que está em D3Dcommon. h. Por exemplo, para nomear pTexture com um nome SDKLayer de mytexture.jpg, use o seguinte código:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



Normalmente, você deve compilar essas chamadas fora de sua versão de produção.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 