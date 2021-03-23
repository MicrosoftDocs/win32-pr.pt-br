---
title: Trabalhando com o Direct3D 11, o Direct3D 10 e o Direct2D
description: Esta seção aborda técnicas de interoperabilidade com versões anteriores do Direct3D e Direct2D, a API do Direct3D 11on12 e diretrizes de portabilidade do Direct3D 11 para o Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103433"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a>Trabalhando com o Direct3D 11, o Direct3D 10 e o Direct2D

Esta seção aborda técnicas de interoperabilidade com versões anteriores do Direct3D e Direct2D, a API do Direct3D 11on12 e diretrizes de portabilidade do Direct3D 11 para o Direct3D 12.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interoperabilidade do Direct3D 12](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | D3D12 pode ser usado para gravar aplicativos divididos em componentes. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Direct3D 11 on 12](direct3d-11-on-12.md)<br/>                                             | D3D11On12 é um mecanismo pelo qual os desenvolvedores podem usar interfaces e objetos do D3D11 para direcionar a API D3D12. O D3D11on12 permite que os componentes escritos usando D3D11 (por exemplo, texto e interface do usuário D2D) trabalhem em conjunto com os componentes criados direcionando a API do D3D12. O D3D11on12 também permite portabilidade incremental de um aplicativo do D3D11 para o D3D12, permitindo que partes do aplicativo continuem direcionando para a D3D11 para simplificar enquanto outras voltam a D3D12 para desempenho, enquanto sempre têm renderização completa e correta. O D3D11On12 torna mais simples do que usar técnicas de interoperabilidade para compartilhar recursos e sincronizar o trabalho entre as duas APIs. <br/> |
| [Portar do Direct3D 11 para o Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)<br/> | Esta seção fornece algumas diretrizes sobre como portar de um mecanismo de gráficos do Direct3D 11 personalizado para o Direct3D 12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

 





