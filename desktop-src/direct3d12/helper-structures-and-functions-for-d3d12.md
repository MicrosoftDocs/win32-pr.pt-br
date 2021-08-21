---
title: Estruturas auxiliares e funções para Direct3D 12
description: Essas estruturas auxiliares e funções auxiliares são declaradas em `d3dx12.h` .
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Funções auxiliares
- Estruturas auxiliares
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b42bc9ae73f3537cc786a465feba596b3392401
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812175"
---
# <a name="helper-structures-and-functions-for-direct3d-12"></a>Estruturas auxiliares e funções para Direct3D 12

Essas estruturas auxiliares e funções auxiliares são declaradas em `d3dx12.h` .

`d3dx12.h` está disponível separadamente dos headers do Direct3D 12. Você pode baixar `d3dx12.h` da [Biblioteca auxiliar D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

Você pode usar essas estruturas auxiliares para criar e inicializar estruturas Direct3D. Essas estruturas auxiliares se comportam como classes C++. Cada estrutura auxiliar normalmente tem um construtor padrão, um construtor explícito, um destruidor e um operador de cast para a estrutura D3D12 associada. Cada estrutura auxiliar tem um prefixo 'C' e está associada a uma estrutura D3D12 que não tem o prefixo 'C'. A maioria das estruturas auxiliares contém métodos de membro de inicialização, alguns contêm funções de comparação.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [Interfaces auxiliares do D3D12](helper-interfaces-for-d3d12.md) | Essas interfaces auxiliares ajudam principalmente no tratamento de sub-recursos e são declaradas em `d3dx12.h` .  |
| [Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md) | Essas estruturas auxiliares ajudam a inicializar muitas das estruturas do Direct3D 12 e são declaradas em `d3dx12.h` . |
| [Funções auxiliares do D3D12](helper-functions-for-d3d12.md) | Essas funções auxiliares ajudam principalmente no tratamento de sub-recursos e são declaradas em `d3dx12.h` .  |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência do Direct3D 12](direct3d-12-reference.md)
