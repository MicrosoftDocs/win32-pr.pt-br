---
description: Esta seção especifica os formatos ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 11,1.
ms.assetid: 90EADE0C-A984-4993-A3F8-D045C535DE64
title: Suporte de formato para hardware 11.1 do Nível de Recursos do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999228224ebd88c234f46eaa719275fb6cf9bce8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564230"
---
# <a name="format-support-for-direct3d-feature-level-111-hardware"></a>Suporte de formato para hardware 11.1 do Nível de Recursos do Direct3D

Esta seção especifica os formatos ([_* DXGI_FORMAT_* * _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) que têm suporte no hardware do nível de recurso do Direct3D 11,1.

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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>PCs</sup> não tipados (1)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>\_<sup>FCS</sup> de DXGI_FORMAT_R32G32B32A32 float (2)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>\_<sup>FCS</sup> DXGI_FORMAT_R32G32B32A32 uint (3)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ Santo<sup>FCS</sup> (4)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 \_ <sup>PCs</sup> não tipados (5)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>\_<sup>FCS</sup> de DXGI_FORMAT_R32G32B32 float (6)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![opcionais](images/letter-o.jpg) |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>\_<sup>FCS</sup> DXGI_FORMAT_R32G32B32 uint (7)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32 \_ Santo<sup>FCS</sup> (8)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>PCs</sup> não tipados (9)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>\_<sup>FCS</sup> de DXGI_FORMAT_R16G16B16A16 float (10)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a>\_<sup>FCS</sup> DXGI_FORMAT_R16G16B16A16 UNORM (11)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a>\_<sup>FCS</sup> DXGI_FORMAT_R16G16B16A16 uint (12)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a>\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16B16A16 (13)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ Santo<sup>FCS</sup> (14)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 \_ <sup>PCs</sup> não tipados (15)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>\_<sup>FCS</sup> de DXGI_FORMAT_R32G32 float (16)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a>\_<sup>FCS</sup> DXGI_FORMAT_R32G32 uint (17)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32 \_ Santo<sup>FCS</sup> (18)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 \_ <sup>PCs</sup> não tipados (19)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a>DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint do<sup>FCS</sup> (20)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a>\_FCS DXGI_FORMAT_R32 \_ \_ de tipo float<sup></sup> X8X24 (21)
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
| Exemplo de sombreador \_ c (filtro de comparação) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | ![exigido](images/letter-r.jpg) |
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

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a>\_ \_ G8X24 \_ de<sup>FCS</sup> (22) não tipado DXGI_FORMAT_X32
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>PCs</sup> não tipados (23)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R10G10B10A2 (24)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>\_<sup>FCS</sup> DXGI_FORMAT_R10G10B10A2 uint (25)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM<sup>FCS</sup> (89)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>PCs</sup> não tipados (27)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8B8A8 (28)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a>\_FCS DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup></sup> sRGB (29)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a>\_<sup>FCS</sup> DXGI_FORMAT_R8G8B8A8 uint (30)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>FCS</sup> SNORM (31)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>\_<sup>FCS</sup> DXGI_FORMAT_R8G8B8A8 Santo (32)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ <sup>PCs</sup> não tipados (33)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>\_<sup>FCS</sup> de DXGI_FORMAT_R16G16 float (34)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16 (35)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>\_<sup>FCS</sup> DXGI_FORMAT_R16G16 uint (36)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16G16 (37)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>\_<sup>FCS</sup> DXGI_FORMAT_R16G16 Santo (38)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 \_ <sup>PCs</sup> não tipados (39)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>\_<sup>FCS</sup> de DXGI_FORMAT_D32 float (40)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>\_<sup>FCS</sup> de DXGI_FORMAT_R32 float (41)
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
| Exemplo de sombreador \_ c (filtro de comparação) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | ![exigido](images/letter-r.jpg) |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>\_<sup>FCS</sup> DXGI_FORMAT_R32 uint (42)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>\_<sup>FCS</sup> DXGI_FORMAT_R32 Santo (43)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 \_ <sup>PCs</sup> não tipados (44)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a>\_FCS DXGI_FORMAT_D24 \_ UNORM \_ S8<sup></sup> uint (45)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a>\_FCS com \_ \_ tipo de UNORM<sup></sup> x8 (46) DXGI_FORMAT_R24
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
| Exemplo de sombreador \_ c (filtro de comparação) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | ![exigido](images/letter-r.jpg) |
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

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a>\_FCS uint não tipado \_ de DXGI_FORMAT_X24 \_ (47)<sup></sup>
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 \_ <sup>PCs</sup> não tipados (48)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8 (49)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>\_<sup>FCS</sup> DXGI_FORMAT_R8G8 uint (50)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R8G8 (51)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>\_<sup>FCS</sup> DXGI_FORMAT_R8G8 Santo (52)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 \_ <sup>PCs</sup> não tipados (53)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>\_<sup>FCS</sup> de DXGI_FORMAT_R16 float (54)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_D16 (55)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R16 (56)
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
| Exemplo de sombreador \_ c (filtro de comparação) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | ![exigido](images/letter-r.jpg) |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>\_<sup>FCS</sup> DXGI_FORMAT_R16 uint (57)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R16 (58)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>\_<sup>FCS</sup> DXGI_FORMAT_R16 Santo (59)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 \_ <sup>PCs</sup> não tipados (60)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_R8 (61)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>\_<sup>FCS</sup> DXGI_FORMAT_R8 uint (62)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>\_SNORM<sup>FCS</sup> de DXGI_FORMAT_R8 (63)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>\_<sup>FCS</sup> DXGI_FORMAT_R8 Santo (64)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| BackBuffer convertida até mesmo totalmente tipado | \- |
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ <sup>PCC</sup> de tipo (70)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a>DXGI_FORMAT_BC1 \_ UNORM <sup>FCC</sup> (71)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ sRGB <sup>FCC</sup> (72)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ <sup>PCC</sup> de tipo (73)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a>DXGI_FORMAT_BC2 \_ UNORM <sup>FCC</sup> (74)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ sRGB <sup>FCC</sup> (75)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ <sup>PCC</sup> de tipo (76)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a>DXGI_FORMAT_BC3 \_ UNORM <sup>FCC</sup> (77)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ sRGB <sup>FCC</sup> (78)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>PCC</sup> de tipo (79)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a>DXGI_FORMAT_BC4 \_ UNORM <sup>FCC</sup> (80)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a>DXGI_FORMAT_BC4 \_ SNORM <sup>FCC</sup> (81)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ <sup>PCC</sup> de tipo (82)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a>DXGI_FORMAT_BC5 \_ UNORM <sup>FCC</sup> (83)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a>DXGI_FORMAT_BC5 \_ SNORM <sup>FCC</sup> (84)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 \_ <sup>PCs</sup> não tipados (90)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_B8G8R8A8 (87)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>\_FCS DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup></sup> sRGB (91)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 \_ <sup>PCs</sup> não tipados (92)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>\_UNORM<sup>FCS</sup> de DXGI_FORMAT_B8G8R8X8 (88)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>\_FCS DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup></sup> sRGB (93)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a>DXGI_FORMAT_BC6H \_ <sup>PCC</sup> de tipo (94)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a>DXGI_FORMAT_BC6H \_ UF16 <sup>FCC</sup> (95)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a>DXGI_FORMAT_BC6H \_ SF16 <sup>FCC</sup> (96)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a>DXGI_FORMAT_BC7 \_ <sup>PCC</sup> de tipo (97)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a>DXGI_FORMAT_BC7 \_ UNORM <sup>FCC</sup> (98)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a>DXGI_FORMAT_BC7 \_ UNORM \_ sRGB <sup>FCC</sup> (99)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 \_ opaco<sup>V</sup> (106)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
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

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)
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
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 \_ bit \_ ) | \- |
| Gather4 do sombreador | ![exigido](images/letter-r.jpg) |
| Sombreador gather4 \_ c | \- |
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
| Recurso em ladrilho | ![opcionais](images/letter-o.jpg) |

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

## <a name="related-topics"></a>Tópicos relacionados

[Níveis de recursos de hardware do D3D12](../direct3d12/hardware-feature-levels.md)

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
