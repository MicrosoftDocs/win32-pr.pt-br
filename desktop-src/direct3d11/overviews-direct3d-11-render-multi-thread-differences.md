---
title: Diferenças de Threading entre versões do Direct3D
description: Muitos modelos de programação multi-threaded usam primitivos de sincronização (como mutexes) para criar seções críticas e impedir que o código seja acessado por mais de um thread por vez.
ms.assetid: 0c4f984e-4dd0-4714-b911-592ca86d5dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e99c68dbdba1d6f0cdd789f6ccac8b81d4ac03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366342"
---
# <a name="threading-differences-between-direct3d-versions"></a>Diferenças de Threading entre versões do Direct3D

Muitos modelos de programação multi-threaded usam primitivos de sincronização (como mutexes) para criar seções críticas e impedir que o código seja acessado por mais de um thread por vez.

No entanto, os métodos de criação de recursos da interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) foram projetados para serem reentrante, sem a necessidade de primitivos de sincronização e seções críticas. Como resultado, os métodos de criação de recursos são eficientes e fáceis de usar.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 11, o 10 e o 9:<br/> O Direct3D 11 usa como padrão thread-safe e continua a permitir que os aplicativos sejam recusados usando D3D11 \_ criar \_ dispositivo \_ SINGLETHREADED. Se os aplicativos optarem por serem thread-safe, eles deverão aderir às regras de Threading. O tempo de execução sincroniza threads em nome do aplicativo, permitindo a execução de threads simultâneos. Na verdade, a sincronização no Direct3D 11 é mais eficiente do que usar a camada thread-safe no Direct3D 10.<br/> O Direct3D 10 pode dar suporte à execução de apenas um thread por vez. O Direct3D 10 é totalmente seguro para thread e permite que um aplicativo recuse esse comportamento usando D3D10 \_ criar \_ dispositivo \_ único \_ threaded. <br/> O Direct3D 9 não usa como padrão thread-safe. No entanto, ao chamar [**CreateDevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) ou [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) para criar um dispositivo, você pode especificar o \_ sinalizador multithread D3DCREATE para tornar o thread da API do Direct3D 9 seguro. Isso causa uma sobrecarga de sincronização significativa. Portanto, tornar o thread de API do Direct3D 9 seguro não é recomendado porque o desempenho pode ser degradado.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

