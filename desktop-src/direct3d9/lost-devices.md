---
description: Um dispositivo Direct3D pode estar em um estado operacional ou um estado perdido.
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: Dispositivos perdidos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a808cb113f5c2fd35a741e0efc7c6b8af9e127df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296015"
---
# <a name="lost-devices-direct3d-9"></a>Dispositivos perdidos (Direct3D 9)

Um dispositivo Direct3D pode estar em um estado operacional ou um estado perdido. O estado operacional é o estado normal do dispositivo no qual o dispositivo é executado e apresenta toda a renderização conforme o esperado. O dispositivo faz uma transição para o perdido estado quando um evento, como perda de foco do teclado em um aplicativo de tela inteira, faz com que a renderização para se tornar impossível. O estado perdido é caracterizado pela falha silenciosa de todas as operações de renderização, ou seja, os métodos de renderização podem retornar códigos de sucesso mesmo em caso de falha das operações de renderização. Nessa situação, o código de erro D3DERR \_ DEVICELOST é retornado por [**IDirect3DDevice9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

Por padrão, o conjunto completo de cenários que pode provocar a perda do dispositivo não é especificado. Alguns exemplos típicos incluem perda do foco, como quando o usuário pressionar ALT + TAB ou quando uma caixa de diálogo do sistema é inicializada. Os dispositivos também podem ser perdidos devido a um evento de gerenciamento de energia ou quando outro app assume a operação de tela inteira. Além disso, qualquer falha de [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) coloca o dispositivo em um estado perdido.

Todos os métodos derivados de [**IDesconhecido**](/windows/win32/api/unknwn/nn-unknwn-iunknown) têm garantia de funcionar depois que um dispositivo é perdido. Após a perda de dispositivo, cada função geralmente tem três opções:

-   Falha com D3DERR \_ DEVICELOST-isso significa que o aplicativo precisa reconhecer que o dispositivo foi perdido, para que o aplicativo identifique que algo não está acontecendo conforme o esperado.
-   Falha silenciosa, retornando S \_ OK ou qualquer outro código de retorno-se uma função falhar silenciosamente, o aplicativo geralmente não poderá distinguir entre o resultado de "êxito" e uma "falha silenciosa".
-   A função retorna um código de retorno.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Um dispositivo Direct3D 9 retorna D3DERR \_ DEVICELOST. Depois de retornado de [**IDirect3DDevice9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), o comportamento de emulação não funcionará mais e todas as chamadas futuras falharão até que o dispositivo seja redefinido com êxito.<br/> Um dispositivo Direct3D 9Ex nunca retorna D3DERR \_ DEVICELOST, mas pode retornar novas mensagens de status (consulte [alterações de comportamento do dispositivo](dx9lh.md)).<br/> |



 

## <a name="responding-to-a-lost-device"></a>Responder a um dispositivo perdido

Um dispositivo perdido deve recriar recursos (incluindo os recursos de memória de vídeo) depois que for redefinido. Se um dispositivo for perdido, o app consulta o dispositivo para verificar se é possível restaurar o estado operacional. Caso contrário, o app aguarda até que o dispositivo poder ser restaurado.

Se for possível restaurar o dispositivo, o app o prepara ao destruir todos os recursos de memória de vídeo e qualquer cadeias de permuta. Em seguida, o aplicativo chama o método [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) . Reset é o único método que tem um efeito quando um dispositivo é perdido e é o único método pelo qual um aplicativo pode alterar o dispositivo de um estado de operação perdido para um. A redefinição falhará a menos que o aplicativo libere todos os recursos alocados no \_ padrão D3DPOOL, incluindo aqueles criados pelos métodos [**IDirect3DDevice9:: CreateRenderTarget**](/windows/desktop/api) e [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

Na maioria das vezes, as chamadas de alta frequência do Direct3D não retornam informações sobre a perda do dispositivo. O aplicativo pode continuar a chamar métodos de renderização, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), sem receber a notificação de um dispositivo perdido. Internamente, essas operações serão descartadas depois que o dispositivo for redefinido para o estado operacional.

O aplicativo pode determinar o que fazer ao encontrar um dispositivo perdido consultando o valor de retorno do método [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) .

## <a name="locking-operations"></a>Operações de bloqueio

Internamente, o Direct3D trabalha o suficiente para garantir que uma operação de bloqueio será bem-sucedida depois que um dispositivo for perdido. No entanto, não é garantido que os dados do recurso de memória de vídeo serão precisos durante a operação de bloqueio. É garantido que nenhum código de erro será retornado. Isso permite que os apps sejam gravados sem se preocupar com a perda de dispositivo durante uma operação de bloqueio.

## <a name="resources"></a>Recursos

Os recursos podem consumir a memória de vídeo. Como um dispositivo perdido está desconectado da memória de vídeo do adaptador, não é possível garantir a alocação da memória de vídeo quando o dispositivo for perdido. Como resultado, todos os métodos de criação de recursos são implementados com sucesso retornando o D3D \_ OK, mas, na verdade, aloque apenas a memória fictícia do sistema. Como qualquer recurso de memória de vídeo deve ser destruído antes de redimensionar o dispositivo, não há nenhum problema em sobrealocar a memória de vídeo. Essas superfícies fictícias permitem que as operações de bloqueio e de cópia pareçam funcionar normalmente até que o aplicativo chame [**IDirect3DDevice9::P reenviada**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) e descobre que o dispositivo foi perdido.

Toda a memória de vídeo deve ser liberada antes que um dispositivo possa ser restaurado de um estado perdido para operacional. Isso significa que o aplicativo deve liberar qualquer cadeia de permuta criada com [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) e todos os recursos colocados na \_ classe de memória padrão D3DPOOL. O aplicativo não precisa liberar recursos nas classes de \_ memória D3DPOOL Managed ou D3DPOOL \_ SYSTEMMEM. Outros dados de estado são destruídos automaticamente pela transição para um estado operacional.

É recomendado desenvolver apps com um único caminho de código para responder à perda de dispositivo. Esse caminho de código é provavelmente semelhante, ou idêntico, ao caminho de código necessário para inicializar o dispositivo durante a inicialização.

## <a name="retrieved-data"></a>Dados recuperados

O Direct3D permite que os aplicativos validem os Estados de textura e de renderização contra a renderização de passagem única pelo hardware usando [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice). Esse método, que normalmente é invocado durante a inicialização do aplicativo, retornará D3DERR \_ DEVICELOST se o dispositivo tiver sido perdido.

O Direct3D também permite que apps copiem imagens geradas ou gravadas anteriormente de recursos de memória de vídeo para recursos de memória não volátil do sistema. Como as imagens de origem dessas transferências podem ser perdidas a qualquer momento, o Direct3D permite que essas operações de cópia falhem quando o dispositivo for perdido.

Em relação a consultas assíncronas, [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retorna D3DERR \_ DEVICELOST se o sinalizador de liberação for especificado, para indicar ao aplicativo que **IDirect3DQuery9:: GetData** nunca retornará S \_ OK.

A operação de cópia, [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api), pode falhar com D3DERR \_ DEVICELOST, já que não há nenhuma superfície primária quando o dispositivo é perdido. [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) também pode falhar com D3DERR \_ DEVICELOST porque um buffer de fundo não pode ser criado quando o dispositivo é perdido. Observe que esses casos são a única instância de D3DERR \_ DEVICELOST fora dos métodos [**IDirect3DDevice9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)e [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) .

## <a name="programmable-shaders"></a>Sombreadores programáveis

No Direct3D 9, os sombreadores de vértices e os sombreadores de pixel não precisam ser recriados após a redefinição. Eles serão lembrados. Nas versões anteriores do DirectX, um dispositivo perdido os sombreadores necessários para serem recriados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
