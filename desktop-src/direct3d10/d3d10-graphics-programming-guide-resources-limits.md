---
description: Esta tabela contém uma lista dos recursos mínimos com suporte do Direct3D 10.
ms.assetid: 79c13aed-87bd-4875-9810-c3e078f58753
title: Limites de recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ea3e3a181605e548c4e9f0a8b69691564163799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010295"
---
# <a name="resource-limits-direct3d-10"></a>Limites de recursos (Direct3D 10)

Esta tabela contém uma lista dos recursos mínimos com suporte do Direct3D 10.



| Recurso                                                                                               | Limite                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Número de elementos em um buffer de constantes                                                                | 4096                                                 |
| Número de texels (independente do tamanho de struct) em um buffer                                              | 227 texels                                           |
| Dimensão Texture1D U                                                                                  | 8192                                                 |
| Dimensão Texture1DArray                                                                               | 512 fatias de matriz                                     |
| Dimensão U/V do Texture2D                                                                                | 8192                                                 |
| Dimensão Texture2DArray                                                                               | 512 fatias de matriz                                     |
| Dimensão de Texture3D U/V/W                                                                              | 2.048                                                 |
| Dimensão TextureCube                                                                                  | 8192                                                 |
| Tamanho do recurso (em MB)                                                                                  | 128 MB ¹                                              |
| MaxAnisotropy Anisotropic Filtering                                                                    | 16                                                   |
| Dimensão de recursos endereçável por filtragem de hardware                                                   | 8192 por dimensão                                   |
| Tamanho do recurso (em MB) endereçável por IA (dados de entrada ou de vértice) ou VS/GS/PS (exemplo de ponto)              | 128 MB ¹                                              |
| Número total de exibições de recursos por contexto (cada matriz conta como 1) (todos os tipos de exibição têm limite compartilhado) | 220                                                  |
| Tamanho da estrutura do buffer (vários elementos)                                                                  | 2\.048 bytes                                           |
| Tamanho da saída do fluxo                                                                                     | O mesmo que o número de texels em um buffer (veja acima) |
| Contagem de vértices Draw ou DrawInstanced (incluindo instanciação)                                              | 232                                                  |
| \[Contagem de vértices da instância DrawIndexed \] () (incluindo instâncias)                                             | 232                                                  |
| Dados de saída de invocação GS ( \* vértices de componentes)                                                     | 1024                                                 |
| Número total de objetos de amostra por contexto                                                            | 4096                                                 |
| Número total de objetos viewport/recortantes por pipeline                                                  | 16                                                   |
| Número total de distâncias de clip/seleção por vértice                                                         | 8                                                    |
| Número total de objetos de mistura por contexto                                                              | 4096                                                 |
| Número total de objetos de profundidade/estêncil por contexto                                                      | 4096                                                 |
| Número total de objetos de estado do rasterizador por contexto                                                   | 4096                                                 |
| Contagem máxima de amostras por pixel durante a multiamostragem                                                    | 32                                                   |
| Vértice de recursos do sombreador – contagem de elementos (componentes de 4 32 bits)                                          | 16                                                   |
| Common-shader Core (componentes de 4 32 bits) contagem de registro temporário (r \# + indexável x \# \[ n \] )             | 4096                                                 |
| Comum-sombreador-principais slots de buffer                                                               | 14                                                   |
| Entrada de núcleo de sombreador comum – slots de recurso                                                                | 128                                                  |
| Slots de amostra de núcleo de sombreador comum                                                                       | 16                                                   |
| Principal-limite de agrupamento de sub-rotinas de sombreador                                                            | 32                                                   |
| Limite de aninhamento de controle de fluxo principal de sombreador comum                                                          | 64                                                   |
| Entrada do sombreador de vértice-contagem de registros (componentes de 4 32 bits)                                            | 16                                                   |
| Saída do sombreador de vértice-contagem de registros (componentes de 4 32 bits)                                           | 16                                                   |
| Entrada do sombreador de geometria-contagem de registros (componentes de 4 32 bits)                                          | 16                                                   |
| Saída do sombreador de geometria-contagem de registros (componentes de 4 32 bits)                                         | 32                                                   |
| Entrada do sombreador de pixel – contagem de registros (componentes de 4 32 bits)                                             | 32                                                   |
| Saída do sombreador de pixel-contagem de registros (componentes de 4 32 bits)                                            | 8                                                    |
| Contagem de registros de profundidade de saída do sombreador de pixel ( \* 1 – componente de 32 bits)                                          | 1                                                    |
| Slots do recurso de entrada de índice do assembler de entrada                                                             | 1                                                    |
| Slots de recursos de entrada de vértice do assembler de entrada                                                            | 16                                                   |



 

os aplicativos ¹ podem criar recursos maiores do que o tamanho máximo de recursos em alguns hardwares gráficos. No entanto, recomendamos que os aplicativos mantenham recursos menores do que o tamanho máximo do recurso para obter a quantidade máxima de compatibilidade entre fornecedores de gráficos. O tempo de execução garante apenas que as alocações dentro do tamanho máximo do recurso sejam suportadas por todo o hardware do Direct3D 10. Se um aplicativo tentar alocar memória para um recurso dentro do tamanho máximo do recurso, o tempo de execução falhará na tentativa somente se o sistema operacional ficar sem recursos. Se um aplicativo tentar alocar memória para um recurso acima do tamanho máximo do recurso, o tempo de execução poderá falhar na tentativa porque o sistema operacional é estendido ou o hardware não oferece suporte a alocações acima do tamanho máximo do recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



