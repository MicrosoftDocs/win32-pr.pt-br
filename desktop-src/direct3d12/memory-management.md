---
title: Gerenciamento de memória no Direct3D 12
description: A mudança para o D3D12 envolve a sincronização adequada e o gerenciamento da residência de memória.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481801"
---
# <a name="memory-management-in-direct3d-12"></a>Gerenciamento de memória no Direct3D 12

A mudança para o D3D12 envolve a sincronização adequada e o gerenciamento da residência de memória. O gerenciamento de residência de memória significa que ainda mais sincronização deve ser feita. Esta seção aborda as estratégias de gerenciamento de memória e a subalocação dentro de heaps e buffers.

-   [Nesta seção](#in-this-section)
-   [Tópicos relacionados](#related-topics)

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estratégias de gerenciamento de memória](memory-management-strategies.md)<br/> | Um Gerenciador de memória para o Direct3D 12 poderia ficar muito complicado com todas as diferentes camadas de suporte, para adaptadores de uma ou discretos (não de uma) e com uma variedade considerável de diferenças de arquitetura entre os adaptadores de GPU.<br/> A estratégia recomendada para o gerenciamento de memória do Direct3D 12, descrita nesta seção, é "classificar, orçamento e fluxo".<br/> |
| [Subalocação em buffers](large-buffers.md)<br/>                | Os buffers têm todos os recursos necessários no D3D12 para que os aplicativos transfiram uma grande variedade de dados transitórios da CPU para a GPU. Esta seção aborda quatro cenários comuns para o uso e o gerenciamento de recursos e buffers.<br/>                                                                                                                                     |
| [Subalocação em heaps](suballocation-within-heaps.md)<br/>     | Heaps de recursos transferem dados da CPU para a GPU (carregamento) e da GPU para a CPU (leitura de volta). <br/>                                                                                                                                                                                                                                                                  |
| [Residência](residency.md)<br/>                                       | Um objeto é considerado *residente* quando ele é acessível pela GPU.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Associação de recursos](resource-binding.md)
</dt> </dl>

 

 





