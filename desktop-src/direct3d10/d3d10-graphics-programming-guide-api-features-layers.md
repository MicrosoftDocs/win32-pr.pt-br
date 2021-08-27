---
description: Camadas de API (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: Camadas de API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd452032eda61c49edbf007b5ebaf0314f9054fe0b016cf07e3f4473ae3abee6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119986"
---
# <a name="api-layers-direct3d-10"></a>Camadas de API (Direct3D 10)

O runtime do Direct3D 10 é construído com camadas, começando com a funcionalidade básica no núcleo e criando funcionalidades opcionais e de assistência do desenvolvedor em camadas externas.

## <a name="core-layer"></a>Camada principal

A camada principal existe por padrão; fornecendo um mapeamento muito fino entre a API e o driver de dispositivo, minimizando a sobrecarga para chamadas de alta frequência. Como a camada principal é essencial para o desempenho, ela só executa a validação crítica.

As camadas restantes são opcionais. Como regra geral, as camadas adicionam funcionalidade, mas não modificam o comportamento existente. Por exemplo, as funções principais terão os mesmos valores de retorno independentes da camada de depuração que está sendo instautada, embora a saída de depuração adicional possa ser fornecida se a camada de depuração for instautada.

Crie camadas quando um dispositivo for criado chamando [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) e fornecendo um ou mais valores de SINALIZADOR DE DISPOSITIVO [**D3D10 \_ CREATE. \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)

## <a name="debug-layer"></a>Camada de depuração

A camada de depuração fornece uma ampla validação de consistência e parâmetro adicional (como validar vinculação de sombreador e associação de recursos, validar a consistência do parâmetro e relatar descrições de erro). A saída gerada pela camada de depuração consiste em uma fila de cadeias de caracteres que podem ser acessadas usando a [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) (consulte Personalizar a saída de depuração com [ID3D10InfoQueue (Direct3D 10)](d3d10-graphics-programming-guide-api-features-layers-info-queue.md)). Os erros gerados pela camada principal são realçadas com avisos pela camada de depuração.

Para criar um dispositivo que dá suporte à camada de depuração, você deve instalar o SDK do DirectX (para obter D3D10SDKLayers.DLL) e especificar o sinalizador D3D10 CREATE DEVICE DEBUG ao chamar \_ \_ \_ [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice). É claro que a execução de um aplicativo com a camada de depuração será substancialmente mais lenta. Para habilitar/desabilitar mensagens de depuração para APIs D3DX10, chame [**D3DX10DebugMute**](d3dx10debugmute.md).

Quando a camada de depuração lista vazamentos de memória, ela emita uma lista de ponteiros de interface de objeto juntamente com seus nomes amigáveis. O nome amigável padrão é " &lt; sem nome &gt; ". Você pode definir o nome amigável usando o método [**ID3D10DeviceChild::SetPrivateData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) e o GUID **WKPDID \_ D3DDebugObjectName** que está em D3Dcommon.h. Por exemplo, para nomear pTexture com um nome SDKLayer de mytexture.jpg, use o seguinte código:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



Normalmente, você deve compilar essas chamadas da versão de produção.

## <a name="switch-to-reference-layer"></a>Alternar para camada de referência

Essa camada permite que um aplicativo transição entre um dispositivo de hardware (HAL) e um REF (dispositivo de software ou referência). Para alternar um dispositivo, primeiro você deve criar um dispositivo que dá suporte à camada de alternância para referência (consulte [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) e, em seguida, chamar [**ID3D10SwitchToRef::SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref).

Todos os estados, recursos e objetos do dispositivo são mantidos por meio dessa transição de dispositivo. No entanto, às vezes não é possível corresponder exatamente aos dados do recurso. Isso ocorre porque algumas informações estão disponíveis para um dispositivo de hardware que não está disponível para um dispositivo de referência.

Praticamente todos os aplicativos em tempo real usam a implementação de HAL do pipeline. Quando o pipeline é alternado de um dispositivo de hardware para um dispositivo de referência, as operações de renderização são feitas simultaneamente em hardware e software. À medida que o dispositivo de software está renderizar, ele exigirá que os recursos sejam baixados na memória do sistema. Isso pode exigir que outros recursos armazenados em cache na memória do sistema sejam despejados para tornar o espaço.

> [!Note]  
> Esse recurso switch-to-reference-layer tem suporte apenas no Direct3D 10 e direct3D 10.1 e não tem mais suporte no Direct3D 11 e em versões posteriores.

 

## <a name="thread-safe-layer"></a>Thread-Safe camada

Essa camada foi projetada para permitir que aplicativos multi-threaded acessem o dispositivo de vários threads.

Um aplicativo Direct3D 10 pode controlar uma sincronização de dispositivo usando funções de dispositivo. Isso permite que um aplicativo habilita/desabilite seções críticas (habilitando/desabilitando temporariamente a proteção multithreading) e assumir/liberar um bloqueio de seção crítica em vários pontos de entrada da API do Direct3D 10. A camada thread-safe está habilitada por padrão. Para aplicativos de thread único, a camada thread-safe não tem impacto sobre o desempenho.




Diferenças entre o Direct3D 9 e o Direct3D 10:

- Ao contrário do Direct3D 9, a API do Direct3D 10 assume como padrão totalmente thread-safe.



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos da API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




