---
title: Funções auxiliares para Direct3D 12
description: Essas funções auxiliares ajudam particularmente na manipulação de subrecursos e são declaradas em `d3dx12.h` .
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funções auxiliares
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9434bf916d7cb92116cdf4f7f6d86363b2eb51
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813183"
---
# <a name="helper-functions-for-direct3d-12"></a>Funções auxiliares para Direct3D 12

Essas funções auxiliares ajudam particularmente na manipulação de subrecursos e são declaradas em `d3dx12.h` .

`d3dx12.h` está disponível separadamente dos cabeçalhos do Direct3D 12. Você pode baixar `d3dx12.h` da [biblioteca auxiliar do D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**CommandListCast**](commandlistcast.md) | Esse modelo de função converte um ponteiro constante para qualquer lista de comandos em um ponteiro const para um ID3D12CommandList. |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md) | Calcula um índice de subrecurso para uma textura. |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md) | Gera a fatia MIP, a fatia da matriz e a fatia do plano que correspondem ao índice de subrecurso especificado. |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) | Obtém o número de planos para o formato DXGI especificado para o adaptador virtual especificado (um **ID3D12Device**). |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md) | Indica se o layout é opaco. |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md) | Retorna o tipo de subobjeto que corresponde à classe base do tipo de subobjeto passado. |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md) | Analisa uma descrição de fluxo de estado de pipeline, chamando um retorno de chamada definido pelo usuário para cada instância de subobjeto analisada. |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md) | Ajuda a habilitar os recursos da assinatura raiz 1,1 quando eles estão disponíveis e não requer a manutenção de dois caminhos de código para a criação de assinaturas raiz. Esse método auxiliar reconstrói uma assinatura raiz da versão 1,0 quando a versão 1,1 não tem suporte. |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md) | Retorna o tamanho necessário de um buffer a ser usado para carregamento de dados. |
| [**Memcpysubresource**](memcpysubresource.md) | Copia uma linha de subrecurso por linha. |
| [**Updatesubresources**](updatesubresources1.md) | Atualiza os subrecursos, todas as matrizes de subrecurso devem ser preenchidas, normalmente chamando [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). |
| [**Updatesubresources (alocação de heap)**](updatesubresources2.md) | Atualiza os subrecursos com uma implementação de alocação de heap. |
| [**Updatesubresources (alocação de pilha)**](updatesubresources3.md) | Atualiza os subrecursos com uma implementação de alocação de pilha. |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência do Direct3D 12](direct3d-12-reference.md)
* [Estruturas e funções auxiliares do D3D12](helper-structures-and-functions-for-d3d12.md)
