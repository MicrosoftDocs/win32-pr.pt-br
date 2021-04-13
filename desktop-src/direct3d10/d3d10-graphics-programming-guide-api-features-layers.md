---
description: Camadas de API (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: Camadas de API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4427083bdcaf389c4b01b590a1bc3fef7eb878b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370388"
---
# <a name="api-layers-direct3d-10"></a>Camadas de API (Direct3D 10)

O tempo de execução do Direct3D 10 é construído com camadas, começando com a funcionalidade básica no núcleo e criando a funcionalidade opcional e auxiliar de desenvolvedor em camadas externas.

## <a name="core-layer"></a>Camada principal

A camada principal existe por padrão; fornecendo um mapeamento muito fino entre a API e o driver de dispositivo, minimizando a sobrecarga para chamadas de alta frequência. Como a camada principal é essencial para o desempenho, ela executa apenas a validação crítica.

As camadas restantes são opcionais. Como regra geral, as camadas adicionam funcionalidade, mas não modificam o comportamento existente. Por exemplo, as funções principais terão os mesmos valores de retorno independentes da camada de depuração que está sendo instanciada, embora a saída de depuração adicional possa ser fornecida se a camada de depuração for instanciada.

Crie camadas quando um dispositivo for criado chamando [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) e fornecendo um ou mais valores de [**\_ sinalizador de \_ dispositivo \_ d3d10 Create**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) .

## <a name="debug-layer"></a>Camada de depuração

A camada de depuração fornece um parâmetro adicional e validação de consistência (como validação de vínculo de sombreador e vinculação de recursos, validação de consistência de parâmetro e descrições de erro de relatório). A saída gerada pela camada de depuração consiste em uma fila de cadeias de caracteres que são acessíveis usando a [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) (consulte [Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)](d3d10-graphics-programming-guide-api-features-layers-info-queue.md)). Os erros gerados pela camada principal são realçados com avisos pela camada de depuração.

Para criar um dispositivo que dê suporte à camada de depuração, você deve instalar o SDK do DirectX (para obter D3D10SDKLayers.DLL) e, em seguida, especificar o \_ sinalizador de depuração do dispositivo d3d10 Create \_ \_ ao chamar [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice). É claro que a execução de um aplicativo com a camada de depuração será consideravelmente mais lenta. Para habilitar/desabilitar mensagens de depuração para APIs D3DX10, chame [**D3DX10DebugMute**](d3dx10debugmute.md).

Quando a camada de depuração lista vazamentos de memória, ela gera uma lista de ponteiros de interface de objeto junto com seus nomes amigáveis. O nome amigável padrão é " &lt; sem nome &gt; ". Você pode definir o nome amigável usando o método [**ID3D10DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) e o GUID **WKPDID \_ D3DDebugObjectName** que está em D3Dcommon. h. Por exemplo, para nomear pTexture com um nome SDKLayer de mytexture.jpg, use o seguinte código:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



Normalmente, você deve compilar essas chamadas fora de sua versão de produção.

## <a name="switch-to-reference-layer"></a>Alternar para a camada de referência

Essa camada permite que um aplicativo faça a transição entre um dispositivo de hardware (HAL) e uma referência ou um dispositivo de software (REF). Para alternar um dispositivo, você deve primeiro criar um dispositivo que dê suporte à camada de switch-to-reference (consulte [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) e, em seguida, chame [**ID3D10SwitchToRef:: SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref).

Todos os Estados, recursos e objetos do dispositivo são mantidos por meio desta transição de dispositivo. No entanto, às vezes não é possível corresponder exatamente aos dados do recurso. Isso se deve ao fato de que algumas informações estão disponíveis para um dispositivo de hardware que não está disponível para um dispositivo de referência.

Praticamente todos os aplicativos em tempo real usam a implementação de HAL do pipeline. Quando o pipeline é alternado de um dispositivo de hardware para um dispositivo de referência, as operações de renderização são feitas simultaneamente no hardware e no software. Como o dispositivo de software está sendo renderizado, ele exigirá que os recursos sejam baixados na memória do sistema. Isso pode exigir que outros recursos armazenados em cache na memória do sistema sejam removidos para liberar espaço.

> [!Note]  
> Esse recurso de camada para referência só tem suporte no Direct3D 10 e no Direct3D 10,1 e não tem mais suporte no Direct3D 11 e versões posteriores.

 

## <a name="thread-safe-layer"></a>Thread-Safe camada

Essa camada foi projetada para permitir que aplicativos multi-threaded acessem o dispositivo de vários threads.

Um aplicativo do Direct3D 10 pode controlar uma sincronização de dispositivo usando funções de dispositivo. Isso permite que um aplicativo habilite/desabilite seções críticas (habilitando/Desabilitando temporariamente a proteção multithreading) e execute/Libere um bloqueio de seção crítica em vários pontos de entrada da API do Direct3D 10. A camada thread-safe é habilitada por padrão. Para aplicativos de thread único, a camada thread-safe não tem impacto sobre o desempenho.



|                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> Ao contrário do Direct3D 9, o padrão da API do Direct3D 10 é totalmente seguro para thread.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




