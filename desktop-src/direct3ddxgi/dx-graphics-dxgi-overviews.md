---
description: A Microsoft DirectX Graphics Infrastructure (DXGI) gerencia tarefas de baixo nível que podem ser independentes do tempo de execução de gráficos do Direct3D. DXGI fornece uma estrutura comum para várias versões do Direct3D.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Guia de programação para DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0ac41155557c14ca41f8e0ea9f1836247bd3b78da213c1fbbed521499eae7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518379"
---
# <a name="programming-guide-for-dxgi"></a>Guia de programação para DXGI

A Microsoft DirectX Graphics Infrastructure (DXGI) gerencia tarefas de baixo nível que podem ser independentes do tempo de execução de gráficos do Direct3D. DXGI fornece uma estrutura comum para várias versões do Direct3D.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                              | Descrição                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral do DXGI](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | Este tópico inclui as seções a seguir.<br/>                                                                                                                   |
| [Aprimoramentos de DXGI 1,2](dxgi-1-2-improvements.md)<br/>                                                                      | A funcionalidade a seguir foi adicionada em DXGI 1,2.<br/>                                                                                                       |
| [Aprimoramentos de DXGI 1,3](dxgi-1-3-improvements.md)<br/>                                                                      | A funcionalidade a seguir foi adicionada no DXGI 1,3, que está incluído a partir do Windows 8.1.<br/>                                                            |
| [Aprimoramentos de DXGI 1,4](dxgi-1-4-improvements.md)<br/>                                                                      | A funcionalidade a seguir foi adicionada ou alterada em DXGI 1,4, em grande parte para dar suporte ao Direct3D 12. <br/>                                                           |
| [Aprimoramentos de DXGI 1,5](dxgi-1-5-improvements.md)<br/>                                                                      | A funcionalidade a seguir foi adicionada ao DXGI 1,5 para dar suporte à especificação e à duplicação de formatos de saída mais flexíveis.<br/>                                |
| [Aprimoramentos de DXGI 1,6](dxgi-1-6-improvements.md)<br/>                                                                      | A funcionalidade a seguir foi adicionada ao DXGI 1,6 para detectar exibições HDR.<br/>                                                                       |
| [Usar DirectX com exibições de alto alcance dinâmico e cor avançada](../direct3darticles/high-dynamic-range.md)     | este tópico fornece uma visão geral técnica da renderização do conteúdo do direct3d 11 e do direct3d 12 de intervalo dinâmico para uma exibição HDR10 usando Windows 10 suporte a cores avançado.<br/> |
| [Exibição da taxa de atualização da variável](variable-refresh-rate-displays.md)<br/>                                                    | As exibições da taxa de atualização da variável exigem que a *divisão* seja habilitada, isso também é conhecido como suporte "vsync-off".<br/>                                                    |
| [Usando a correção gama](using-gamma-correction.md)<br/>                                                                    | A correção gama, ou gama, para curto, é o nome de uma operação não linear que os sistemas usam para codificar e decodificar valores de pixel em imagens.<br/>                        |
| [Suporte de formato para o hardware do recurso Direct3D 10Level9 9,1](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | Esta seção especifica os formatos (valores de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que têm suporte no hardware do recurso Direct3D 10Level9 9,1.<br/>        |
| [Suporte de formato para o hardware do recurso Direct3D 10Level9 9,3](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | Esta seção especifica os formatos (valores de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que têm suporte no hardware do recurso Direct3D 10Level9 9,3.<br/>        |
| [Suporte de formato para hardware 10,0 de nível de recurso Direct3D](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | Esta seção especifica os formatos (valores de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que têm suporte no hardware do Direct3D 10,0.<br/>                        |
| [Suporte de formato para hardware 10,1 de nível de recurso Direct3D](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | Esta seção especifica os formatos (valores de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que têm suporte no hardware do Direct3D 10,1.<br/>                        |
| [Suporte de formato para hardware 11,0 de nível de recurso Direct3D](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | Esta seção especifica os formatos (valores de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que têm suporte no hardware do nível de recurso do Direct3D 11,0.<br/>          |
| [Suporte de formato para hardware 11,1 de nível de recurso Direct3D](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | Esta seção especifica os formatos (valores de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que têm suporte no hardware do nível de recurso do Direct3D 11,1.<br/>          |
| [Suporte de formato para hardware 12,0 de nível de recurso Direct3D](hardware-support-for-direct3d-12-0-formats.md)<br/>               | Esta seção especifica os formatos (valores de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que têm suporte no hardware do nível de recurso do Direct3D 12,0.<br/>          |
| [Suporte de formato para hardware 12,1 de nível de recurso Direct3D](hardware-support-for-direct3d-12-1-formats.md)<br/>               | Esta seção especifica os formatos (valores de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que têm suporte no hardware do Direct3D 12,1.<br/>                        |
| [Verificando o suporte a recursos de hardware](checking-hardware-feature-support.md)<br/>                                              | Esta seção aborda como verificar o suporte de formato para hardware de nível de recurso do Direct3D usando chamadas à API.<br/>                                                       |
| [Para obter o melhor desempenho, use o modelo de flip DXGI](for-best-performance--use-dxgi-flip-model.md)<br/>                              | Este tópico fornece orientação para desenvolvedores sobre como maximizar o desempenho e a eficiência na pilha de apresentação em versões modernas do Windows.<br/>                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[Referência DXGI](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[DXGI (infra-estrutura de gráficos do DirectX): práticas recomendadas](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
