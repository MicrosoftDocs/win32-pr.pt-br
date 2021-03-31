---
description: Esta seção especifica os formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 12,1.
ms.assetid: 0DC50FF3-3193-4F3B-9976-EE504C6FCC87
title: Suporte de formato para hardware 12.1 do Nível de Recursos do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d20b00a2cfb5b0343a2ebb1a56a1253ddd1966
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645618"
---
# <a name="format-support-for-direct3d-feature-level-121-hardware"></a>Suporte de formato para hardware 12.1 do Nível de Recursos do Direct3D

Esta seção especifica os formatos ([_* DXGI_FORMAT_* * _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 12,1.

A tabela resume o suporte a recursos, usando a chave a seguir.

| Símbolo                            | Descrição                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| _ *-**                             | Não permitido ou não disponível.                                                  |
| ![exigido](images/letter-r.jpg)  | O suporte a hardware é necessário.                                                 |
| ![opcionais](images/letter-o.jpg)  | Suporte a hardware opcional, o formato pode ou não ser acelerado por hardware. |
| ![dependentes](images/letter-d.jpg) | Necessário se houver suporte para o recurso opcional relacionado.                            |

Este tópico contém uma seção por formato. Um *destino* de formato (as tabelas contêm uma linha por destino) pode ser um tipo de recurso, uma função intrínseca HLSL ou uma funcionalidade específica que depende de um formato específico.

Para verificar programaticamente o suporte a Format em D3D11 e D3D12, consulte [verificando o suporte a recursos de hardware](checking-hardware-feature-support.md).

> [!NOTE] 
> Os números dos formatos são principalmente, mas nem todos, em ordem numérica crescente &mdash; alguns estão fora de ordem numérica e listados junto com outros formatos relevantes. Observe também que sem *tipo* em um nome de formato pode significar digitação *parcial* e não estritamente tipado (consulte a seção [observações de formato](#format-notes) no final do tópico).

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 0 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | ![exigido](images/letter-r.jpg) |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><sup>Computadores</sup> DXGI_FORMAT_R32G32B32A32_TYPELESS (1)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><sup>Computadores</sup> DXGI_FORMAT_R32G32B32_TYPELESS (5)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 96 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 96 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![opcionais](images/letter-o.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![opcionais](images/letter-o.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![opcionais](images/letter-o.jpg) |
| RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget blendable | ![dependentes](images/letter-d.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![dependentes](images/letter-d.jpg) |
| RenderTarget de multiamostra 8x | ![dependentes](images/letter-d.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 96 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![dependentes](images/letter-d.jpg) |
| RenderTarget de multiamostra 8x | ![dependentes](images/letter-d.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 96 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![dependentes](images/letter-d.jpg) |
| RenderTarget de multiamostra 8x | ![dependentes](images/letter-d.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><sup>Computadores</sup> DXGI_FORMAT_R16G16B16A16_TYPELESS (9)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><sup>FCS</sup> DXGI_FORMAT_R16G16B16A16_UNORM (11)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><sup>FCS</sup> DXGI_FORMAT_R16G16B16A16_UINT (12)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><sup>FCS</sup> DXGI_FORMAT_R16G16B16A16_SNORM (13)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><sup>FCS</sup> DXGI_FORMAT_R16G16B16A16_SINT (14)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><sup>Computadores</sup> DXGI_FORMAT_R32G32_TYPELESS (15)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><sup>FCS</sup> DXGI_FORMAT_R32G32_UINT (17)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssupvsup-19"></a>DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupvsup-20"></a>DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | ![exigido](images/letter-r.jpg) |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupvsup-21"></a>DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | ![exigido](images/letter-r.jpg) |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupvsup-22"></a>DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><sup>Computadores</sup> DXGI_FORMAT_R10G10B10A2_TYPELESS (23)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><sup>FCS</sup> DXGI_FORMAT_R10G10B10A2_UNORM (24)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><sup>Computadores</sup> DXGI_FORMAT_R8G8B8A8_TYPELESS (27)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><sup>FCS</sup> DXGI_FORMAT_R8G8B8A8_UNORM (28)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><sup>FCS</sup> DXGI_FORMAT_R8G8B8A8_UNORM_SRGB (29)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><sup>FCS</sup> DXGI_FORMAT_R8G8B8A8_UINT (30)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><sup>Computadores</sup> DXGI_FORMAT_R16G16_TYPELESS (33)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><sup>Computadores</sup> DXGI_FORMAT_R32_TYPELESS (39)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | ![exigido](images/letter-r.jpg) |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | ![exigido](images/letter-r.jpg) |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | ![exigido](images/letter-r.jpg) |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | ![exigido](images/letter-r.jpg) |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | ![exigido](images/letter-r.jpg) |
| Ops bits UAV atômicas | ![exigido](images/letter-r.jpg) |
| UAV Atomic CMP&Store/CMP&Exch | ![exigido](images/letter-r.jpg) |
| Troca atômica UAV | ![exigido](images/letter-r.jpg) |
| Mínimo de UAV assinado por Atomic/Max | ![exigido](images/letter-r.jpg) |
| UAV atômico sem sinal mínimo/máximo | ![exigido](images/letter-r.jpg) |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | ![exigido](images/letter-r.jpg) |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | ![exigido](images/letter-r.jpg) |
| Ops bits UAV atômicas | ![exigido](images/letter-r.jpg) |
| UAV Atomic CMP&Store/CMP&Exch | ![exigido](images/letter-r.jpg) |
| Troca atômica UAV | ![exigido](images/letter-r.jpg) |
| Mínimo de UAV assinado por Atomic/Max | ![exigido](images/letter-r.jpg) |
| UAV atômico sem sinal mínimo/máximo | ![exigido](images/letter-r.jpg) |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typelesssupvsup-44"></a>DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupvsup-45"></a>DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | ![exigido](images/letter-r.jpg) |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupvsup-46"></a>DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | ![exigido](images/letter-r.jpg) |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupvsup-47"></a>DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><sup>Computadores</sup> DXGI_FORMAT_R8G8_TYPELESS (48)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><sup>Computadores</sup> DXGI_FORMAT_R16_TYPELESS (53)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | ![exigido](images/letter-r.jpg) |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | ![exigido](images/letter-r.jpg) |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><sup>Computadores</sup> DXGI_FORMAT_R8_TYPELESS (60)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | ![exigido](images/letter-r.jpg) |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![exigido](images/letter-r.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | \- |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a>DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a>DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a>DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a>DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a>DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a>DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a>DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a>DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a>DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a>DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![opcionais](images/letter-o.jpg) |
| Buffer de vértice do assembler de entrada | ![opcionais](images/letter-o.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![opcionais](images/letter-o.jpg) |
| Armazenamento digitado UAV | ![opcionais](images/letter-o.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![exigido](images/letter-r.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![opcionais](images/letter-o.jpg) |
| Buffer de vértice do assembler de entrada | ![opcionais](images/letter-o.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![opcionais](images/letter-o.jpg) |
| RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget blendable | ![opcionais](images/letter-o.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![opcionais](images/letter-o.jpg) |
| Armazenamento digitado UAV | ![opcionais](images/letter-o.jpg) |
| Carga digitada UAV | ![opcionais](images/letter-o.jpg) |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![opcionais](images/letter-o.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><sup>Computadores</sup> DXGI_FORMAT_B8G8R8A8_TYPELESS (90)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><sup>Computadores</sup> DXGI_FORMAT_B8G8R8X8_TYPELESS (92)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | ![exigido](images/letter-r.jpg) |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | ![exigido](images/letter-r.jpg) |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget de multiamostra 8x | ![exigido](images/letter-r.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | ![exigido](images/letter-r.jpg) |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a>DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a>DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a>DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a>DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a>DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a>DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | ![exigido](images/letter-r.jpg) |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![exigido](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![exigido](images/letter-r.jpg) |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | \- |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![exigido](images/letter-r.jpg) |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | ![exigido](images/letter-r.jpg) |
| RenderTarget blendable | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | ![exigido](images/letter-r.jpg) |
| Armazenamento digitado UAV | ![exigido](images/letter-r.jpg) |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Sombreador LD | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Sample_c do sombreador (filtro de comparação) | \- |
| Exemplo de sombreador (mono 1_bit_filter) | \- |
| Gather4 do sombreador | \- |
| Gather4_c do sombreador | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV e SRV brutos | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Troca atômica UAV | \- |
| Mínimo de UAV assinado por Atomic/Max | \- |
| UAV atômico sem sinal mínimo/máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | \- |

## <a name="format-notes"></a>Observações de formato

A finalidade do formato pode mudar de um nível de recurso de hardware para o próximo.

<dl> <dt>

<sup>L</sup> : formato de tipo informativo
</dt> <dt>

<sup>PCs</sup> : layout de tipo parcial, convertido e simples
</dt> <dt>

 <sup>FCS</sup> : layout totalmente tipado, convertido e simples
</dt> <dt>

<sup>FNS</sup> : layout totalmente tipado, não-convertido e simples
</dt> <dt>

<sup>PCC</sup> : layout complexo, convertido e de tipo parcial
</dt> <dt>

 <sup>FCC</sup> : layout totalmente tipado, convertido e complexo
</dt> <dt>

<sup>FNC</sup> : layout totalmente tipado, não-convertido e complexo
</dt> <dt>

<sup>V</sup> : formato de vídeo
</dt> </dl>

## <a name="dxgi_format_related-topics"></a>Tópicos de DXGI_FORMAT_Related

[Níveis de recursos de hardware do D3D12](../direct3d12/hardware-feature-levels.md)

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
