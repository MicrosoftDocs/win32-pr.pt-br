---
title: Funções auxiliares do D3D12
description: Essas funções auxiliares ajudam particularmente na manipulação de subrecursos e são declaradas em d3dx12. h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funções auxiliares
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798366"
---
# <a name="helper-functions-for-d3d12"></a>Funções auxiliares do D3D12

Essas funções auxiliares ajudam particularmente na manipulação de subrecursos e são declaradas em **d3dx12. h**.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](cd3dx12-shader-bytecode.md)<br/>                                     | Esse modelo de função converte um ponteiro constante para qualquer lista de comandos em um ponteiro const para um ID3D12CommandList.<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | Calcula um índice de subrecurso para uma textura. <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | Gera a fatia MIP, a fatia da matriz e a fatia do plano que correspondem ao índice de subrecurso especificado. <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | Obtém o número de planos para o formato DXGI especificado para o adaptador virtual especificado (um **ID3D12Device**). <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | Indica se o layout é opaco.<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | Retorna o tipo de subobjeto que corresponde à classe base do tipo de subobjeto passado.<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | Analisa uma descrição de fluxo de estado de pipeline, chamando um retorno de chamada definido pelo usuário para cada instância de subobjeto analisada.<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | Ajuda a habilitar os recursos da assinatura raiz 1,1 quando eles estão disponíveis e não requer a manutenção de dois caminhos de código para a criação de assinaturas raiz. Esse método auxiliar reconstrói uma assinatura raiz da versão 1,0 quando a versão 1,1 não tem suporte.<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | Retorna o tamanho necessário de um buffer a ser usado para carregamento de dados. <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | Copia uma linha de subrecurso por linha. <br/>                                                                                                                                                                                                               |
| [**Updatesubresources**](updatesubresources1.md)<br/>                                      | Atualiza os subrecursos, todas as matrizes de subrecurso devem ser preenchidas, normalmente chamando [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). <br/>                                                                  |
| [**Updatesubresources (alocação de heap)**](updatesubresources2.md)<br/>                    | Atualiza os subrecursos com uma implementação de alocação de heap. <br/>                                                                                                                                                                                    |
| [**Updatesubresources (alocação de pilha)**](updatesubresources3.md)<br/>                   | Atualiza os subrecursos com uma implementação de alocação de pilha. <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Estruturas e funções auxiliares do D3D12](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





