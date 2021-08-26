---
description: Esta seção especifica os formatos ([**DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) com suporte no hardware direct3D Feature 10Level9 9.3.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Suporte de formato para hardware 9.3 do Nível de 10Recursos9 do Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ad2746ce0d6e277f04783ae7140f3855fa7078e9a50b67d1e52bc827403c4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951272"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a>Suporte de formato para hardware 9.3 do Nível de 10Recursos9 do Direct3D

Esta seção especifica os formatos ([**DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valores) com suporte no hardware direct3D Feature 10Level9 9.3.

A tabela resume o suporte ao recurso usando a chave a seguir.

| Símbolo                            | Descrição                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| **-**                             | Não permitido ou não disponível.                                                  |
| ![exigido](images/letter-r.jpg)  | O suporte de hardware é necessário.                                                 |
| ![opcionais](images/letter-o.jpg)  | Suporte de hardware opcional, o formato pode ou não ser acelerado por hardware. |
| ![Dependente](images/letter-d.jpg) | Necessário se há suporte para o recurso opcional relacionado.                            |

Este tópico contém uma seção por formato. Um *destino* de formato (as tabelas contêm uma linha por destino) pode ser um tipo de recurso, uma função intrínseca HLSL ou uma funcionalidade específica que depende de um formato específico.

Para verificar programaticamente o suporte ao formato em D3D11 e D3D12, consulte Verificando o suporte ao [recurso de hardware](checking-hardware-feature-support.md).

> [!NOTE] 
> Os números dos formatos são principalmente, mas não todos, em ordem numérica crescente, alguns estão fora de ordem numérica e listados junto com outros &mdash; formatos relevantes. Observe também que *sem tipo* em  um nome de formato pode significar [](#format-notes) parcialmente digitado e não estritamente sem tipo (consulte a seção Notas de formato no final do tópico).

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 0 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>PCS SEM TIPO</sup> (1)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>FNS FLOAT</sup> (2)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | ![exigido](images/letter-r.jpg) |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | ![exigido](images/letter-r.jpg) |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | ![opcionais](images/letter-o.jpg) |
| 8x RenderTarget multisample | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | ![exigido](images/letter-r.jpg) |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>FNS UINT</sup> (3)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ Santo<sup>FNS</sup> (4)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 128 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 \_ <sup>PCs</sup> não tipados (5)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 96 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a>DXGI_FORMAT_R32G32B32 \_ <sup>FNS FLOAT</sup> (6)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 96 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | ![exigido](images/letter-r.jpg) |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | ![Dependente](images/letter-d.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | ![Dependente](images/letter-d.jpg) |
| 8x RenderTarget multisample | ![Dependente](images/letter-d.jpg) |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a>DXGI_FORMAT_R32G32B32 \_ <sup>FNS UINT</sup> (7)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 96 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
| 4x multiamostrar RenderTarget | ![dependentes](images/letter-d.jpg) |
| RenderTarget de multiamostra 8x | ![dependentes](images/letter-d.jpg) |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a>DXGI_FORMAT_R32G32B32 \_ Santo<sup>FNS</sup> (8)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 96 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
| 4x multiamostrar RenderTarget | ![dependentes](images/letter-d.jpg) |
| RenderTarget de multiamostra 8x | ![dependentes](images/letter-d.jpg) |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>PCs</sup> não tipados (9)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>FNS FLOAT</sup> (10)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | ![exigido](images/letter-r.jpg) |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![opcionais](images/letter-o.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | ![exigido](images/letter-r.jpg) |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | ![opcionais](images/letter-o.jpg) |
| 8x RenderTarget multisample | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)
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
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ Santo<sup>FNS</sup> (14)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 \_ <sup>PCS SEM TIPO</sup> (15)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a>DXGI_FORMAT_R32G32 \_ <sup>FNS FLOAT</sup> (16)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | ![exigido](images/letter-r.jpg) |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | ![opcionais](images/letter-o.jpg) |
| 8x RenderTarget multisample | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | ![exigido](images/letter-r.jpg) |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a>DXGI_FORMAT_R32G32 \_ UINT<sup>FNS</sup> (17)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a>DXGI_FORMAT_R32G32 \_ SINT<sup>FNS</sup> (18)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 \_ <sup>PCs</sup> não tipados (19)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a>DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a>DXGI_FORMAT_R32 FNS SEM TIPO \_ FLOAT \_ X8X24 \_ (21)<sup></sup>
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a>DXGI_FORMAT_X32 \_ \_ FNS UINT G8X24 SEM TIPO \_ (22)<sup></sup>
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 64 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>PCs</sup> não tipados (23)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ UINT<sup>FNS</sup> (25)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a>DXGI_FORMAT_R10G10B10 \_ FNS UNORM DE DESVIO \_ \_ XR A2 \_ (89)<sup></sup>
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>PCs</sup> não tipados (27)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>FNS</sup> UNORM (28)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | ![exigido](images/letter-r.jpg) |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | ![exigido](images/letter-r.jpg) |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | ![opcionais](images/letter-o.jpg) |
| 8x RenderTarget multisample | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | ![exigido](images/letter-r.jpg) |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (29)
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
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | \- |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31)
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
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ Santo<sup>FNS</sup> (32)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ <sup>PCs</sup> não tipados (33)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a>DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | ![exigido](images/letter-r.jpg) |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | ![opcionais](images/letter-o.jpg) |
| 8x RenderTarget multisample | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | ![exigido](images/letter-r.jpg) |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a>DXGI_FORMAT_R16G16 \_ <sup>FNS</sup> UNORM (35)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | ![exigido](images/letter-r.jpg) |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a>DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a>DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | \- |
| RenderTarget | \- |
| RenderTarget blendable | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a>DXGI_FORMAT_R16G16 \_ SINT<sup>FNS</sup> (38)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | ![exigido](images/letter-r.jpg) |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 \_ <sup>PCS SEM TIPO</sup> (39)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a>DXGI_FORMAT_D32 \_ <sup>FNS FLOAT</sup> (40)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a>DXGI_FORMAT_R32 \_ <sup>FNS FLOAT</sup> (41)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | ![exigido](images/letter-r.jpg) |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de mipmap | ![exigido](images/letter-r.jpg) |
| RenderTarget | ![exigido](images/letter-r.jpg) |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a>DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | ![exigido](images/letter-r.jpg) |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a>DXGI_FORMAT_R32 \_ Santo<sup>FNS</sup> (43)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 \_ <sup>PCs</sup> não tipados (44)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a>DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | ![exigido](images/letter-r.jpg) |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | ![opcionais](images/letter-o.jpg) |
| 8x RenderTarget multisample | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a>DXGI_FORMAT_R24 FNS SEM TIPO \_ UNORM \_ X8 \_ (46)<sup></sup>
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a>DXGI_FORMAT_X24 \_ \_ \_ <sup>FNS</sup> UINT G8 SEM TIPO (47)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 \_ <sup>PCs</sup> não tipados (48)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a>DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)
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
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de mipmap | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a>DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a>DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51)
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
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a>DXGI_FORMAT_R8G8 \_ Santo<sup>FNS</sup> (52)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 \_ <sup>PCs</sup> não tipados (53)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a>DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a>DXGI_FORMAT_D16 \_ <sup>FNS</sup> UNORM (55)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | ![exigido](images/letter-r.jpg) |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | ![opcionais](images/letter-o.jpg) |
| 8x RenderTarget multisample | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a>DXGI_FORMAT_R16 \_ <sup>FNS</sup> UNORM (56)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a>DXGI_FORMAT_R16 \_ UINT<sup>FNS</sup> (57)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | ![exigido](images/letter-r.jpg) |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a>DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a>DXGI_FORMAT_R16 \_ SINT<sup>FNS</sup> (59)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 \_ <sup>PCS SEM TIPO</sup> (60)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a>DXGI_FORMAT_R8 \_ <sup>FNS</sup> UNORM (61)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | \- |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a>DXGI_FORMAT_R8 \_ UINT<sup>FNS</sup> (62)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a>DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a>DXGI_FORMAT_R8 \_ SINT<sup>FNS</sup> (64)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ <sup>FNS</sup> UNORM (65)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ <sup>PCC</sup> de tipo (70)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 4 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a>DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 4 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FNC</sup> (72)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 4 |
| Suporte de formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso lado a lado | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ <sup>PCC</sup> SEM TIPO (73)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a>DXGI_FORMAT_BC2 \_ <sup>FNC</sup> UNORM (74)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento digitado UAV | \- |
| Carga digitada UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FNC</sup> (75)
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
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ <sup>PCC</sup> de tipo (76)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a>DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)
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
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FNC</sup> (78)
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
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>PCC</sup> de tipo (79)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 4 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a>DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 4 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a>DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 4 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ <sup>PCC</sup> SEM TIPO (82)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a>DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a>DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)
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
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | ![exigido](images/letter-r.jpg) |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ <sup>FNS</sup> UNORM (86)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 \_ <sup>PCS SEM TIPO</sup> (90)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | \- |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| Adição atômica de UAV | \- |
| Ops bits UAV atômicas | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
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
| Recurso em ladrilho | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)
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
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | \- |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRGB<sup>FNS</sup> (91)
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
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (somente de ponto de amostra) | ![exigido](images/letter-r.jpg) |
| Amostra de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | \- |
| Exibir Scan-Out | ![exigido](images/letter-r.jpg) |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 \_ <sup>PCs</sup> não tipados (92)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte de formato | \- |
| Buffer | \- |
| Buffer de vértice do assembler de entrada | \- |
| Buffer de índice do assembler de entrada | \- |
| Buffer de saída de fluxo | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | \- |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ <sup>FNS</sup> UNORM (88)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | ![exigido](images/letter-r.jpg) |
| Rendertarget | ![exigido](images/letter-r.jpg) |
| Blendable RenderTarget | ![exigido](images/letter-r.jpg) |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | ![opcionais](images/letter-o.jpg) |
| 8x RenderTarget multisample | ![opcionais](images/letter-o.jpg) |
| Outros RT de Contagem Multisample | ![opcionais](images/letter-o.jpg) |
| Resolução multisample | ![exigido](images/letter-r.jpg) |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso lado a lado | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FNS</sup> (93)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | ![exigido](images/letter-r.jpg) |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | ![opcionais](images/letter-o.jpg) |
| RenderTarget de multiamostra 8x | ![opcionais](images/letter-o.jpg) |
| Outros RT de contagem multiamostrais | ![opcionais](images/letter-o.jpg) |
| Resolução de multiamostras | ![exigido](images/letter-r.jpg) |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Converter no layout de bit | \- |
| Suporte a decodificador de vídeo | \- |
| Entrada do processador de vídeo | \- |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | ![exigido](images/letter-r.jpg) |
| Recurso em ladrilho | \- |

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
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | \- |
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
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | \- |
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
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução de multiamostras | \- |
| Carga de multiamostra | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | \- |
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
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | \- |
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
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
| Gather4 do sombreador | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | \- |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | ![exigido](images/letter-r.jpg) |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 32 |
| Suporte ao formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | ![opcionais](images/letter-o.jpg) |
| Entrada do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Saída do processador de vídeo | ![opcionais](images/letter-o.jpg) |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

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
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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
| Recurso Compartilhado | \- |
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
| Amostra de sombreador (somente de ponto de amostra) | \- |
| Amostra de sombreador (qualquer filtro) | \- |
| Exemplo de sombreador \_ c (filtro de comparação) | \- |
| Amostra de sombreador (filtro mono de 1 bit) | \- |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
| Bloqueáveis de CPU | ![exigido](images/letter-r.jpg) |
| 4x multiamostrar RenderTarget | \- |
| RenderTarget de multiamostra 8x | \- |
| Outros RT de contagem multiamostrais | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 8 |
| Suporte ao formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | ![opcionais](images/letter-o.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemplo de sombreador (somente amostra de ponto) | \- |
| Exemplo de sombreador (qualquer filtro) | \- |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | \- |
| Geração automática de Mipmap | \- |
| Rendertarget | \- |
| Blendable RenderTarget | \- |
| Operação lógica de fusão de saída | \- |
| Destino de profundidade/estêncil | \- |
| UAV bruto e SRV | \- |
| UAV estruturado e SRV | \- |
| UAV digitado | \- |
| Armazenamento com tipo UAV | \- |
| Carregamento digitado UAV | \- |
| A adicionar atômico UAV | \- |
| Operações bit a bit atômicas UAV | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| Mínimo ou máximo com assinatura atômica UAV | \- |
| Mínimo ou Máximo não Assinado Atômico UAV | \- |
| Bloqueio de CPU | ![exigido](images/letter-r.jpg) |
| RenderTarget 4x Multisample | \- |
| 8x RenderTarget multisample | \- |
| Outros RT de Contagem Multisample | \- |
| Resolução multisample | \- |
| Carregamento de vários exemplos | \- |
| Exibir Scan-Out | \- |
| Cast dentro do layout de bit | \- |
| Suporte ao decodificador de vídeo | \- |
| Entrada do processador de vídeo | ![exigido](images/letter-r.jpg) |
| Saída do processador de vídeo | \- |
| Recurso Compartilhado | \- |
| Recurso lado a lado | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ <sup>FNS</sup> UNORM (115)
| Destino | Suporte |
| - | - |
| Bits por elemento (BPE) | 16 |
| Suporte ao formato | ![exigido](images/letter-r.jpg) |
| Buffer | \- |
| Buffer de vértice do Assembler de Entrada | \- |
| Buffer de Índice do Assembler de Entrada | \- |
| Buffer de Saída de Fluxo | \- |
| Texture1D | \- |
| Texture2D | ![exigido](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (somente amostra de ponto) | ![exigido](images/letter-r.jpg) |
| Exemplo de sombreador (qualquer filtro) | ![exigido](images/letter-r.jpg) |
| Exemplo de \_ sombreador c (filtro de comparação) | \- |
| Exemplo de sombreador (filtro mono de 1 bits) | \- |
| Sombreador gather4 | \- |
| Sombreador gather4 \_ c | \- |
| Mipmap | ![exigido](images/letter-r.jpg) |
| Geração automática de Mipmap | ![opcionais](images/letter-o.jpg) |
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
| Exchange Atomic UAV | \- |
| UAV com sinal mínimo ou máximo de Atomic | \- |
| UAV atômica não assinado mínimo ou máximo | \- |
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

## <a name="related-topics"></a>Tópicos relacionados

[Níveis de recursos de hardware do D3D12](../direct3d12/hardware-feature-levels.md)

[Implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))

[Mapeando formatos herdados](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
