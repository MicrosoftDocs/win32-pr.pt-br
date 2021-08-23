---
title: Como trabalhar com o Direct2D, o Direct3D 10 e o Direct3D 11
description: Esta seção aborda técnicas de interop com versões anteriores do Direct3D e Direct2D, a API do Direct3D 11on12 e diretrizes de portação do Direct3D 11 para o Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462febfc36c15e2af50f0d4f031bec026bbd8cd3713dafbd9678e733978f484e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989686"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a>Como trabalhar com o Direct2D, o Direct3D 10 e o Direct3D 11

Esta seção aborda técnicas de interop com versões anteriores do Direct3D e Direct2D, a API do Direct3D 11on12 e diretrizes de portação do Direct3D 11 para o Direct3D 12.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interoperabilidade do Direct3D 12](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | D3D12 pode ser usado para escrever aplicativos com componentes. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Direct3D 11 on 12](direct3d-11-on-12.md)<br/>                                             | D3D11On12 é um mecanismo pelo qual os desenvolvedores podem usar interfaces e objetos D3D11 para conduzir a API D3D12. D3D11on12 permite que componentes escritos usando D3D11 (por exemplo, texto D2D e interface do usuário) funcionem em conjunto com componentes gravados destinados à API D3D12. D3D11on12 também permite a portação incremental de um aplicativo de D3D11 para D3D12, permitindo que partes do aplicativo continuem direcionando D3D11 para simplificar, enquanto outros direcionam D3D12 para desempenho, sempre tendo renderização completa e correta. D3D11On12 simplifica o uso de técnicas de interop para compartilhar recursos e sincronizar o trabalho entre as duas APIs. <br/> |
| [Portar do Direct3D 11 para o Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)<br/> | Esta seção fornece algumas diretrizes sobre a portação de um mecanismo gráfico personalizado do Direct3D 11 para o Direct3D 12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

 





