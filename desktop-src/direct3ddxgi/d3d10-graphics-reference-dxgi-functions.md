---
description: Esta seção contém informações sobre as funções fornecidas pelo DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Funções DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500256"
---
# <a name="dxgi-functions"></a>Funções DXGI

Esta seção contém informações sobre as funções fornecidas pelo DXGI.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | Cria uma fábrica de DXGI 1,0 que você pode usar para gerar outros objetos DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | Cria uma fábrica de DXGI 1,1 que você pode usar para gerar outros objetos DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | Cria uma fábrica de DXGI 1,3 que você pode usar para gerar outros objetos DXGI.<br/> No Windows 8, qualquer fábrica de DXGI criado enquanto DXGIDebug.dll estava presente no sistema o carregaria e o usaria. A partir do Windows 8.1, os aplicativos solicitam explicitamente que DXGIDebug.dll sejam carregados em vez disso. Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) e especifique o \_ sinalizador de depuração de criação de fábrica DXGI \_ \_ para solicitar DXGIDebug.dll; a dll será carregada se estiver presente no sistema.<br/> |
| [**DXGIDeclareAdapterRemovalSupport**](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | Permite que um processo indique que ele é resiliente a qualquer um de seus dispositivos gráficos sendo removidos.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | Recupera uma interface de depuração.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DXGIGetDebugInterface1**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | Recupera uma interface que os aplicativos da Windows Store usam para depurar a infraestrutura gráfica do Microsoft DirectX (DXGI).<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




