---
description: Define efeitos de permuta.
ms.assetid: 522a5f71-3ad9-4cfc-a899-e25b9b721b1b
title: Enumeração D3DSWAPEFFECT (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSWAPEFFECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 58354e35ca8456f6fde57d2f2567a6b6a202f6d7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343031"
---
# <a name="d3dswapeffect-enumeration"></a>Enumeração D3DSWAPEFFECT

Define efeitos de permuta.

## <a name="syntax"></a>Sintaxe

```cpp
typedef enum D3DSWAPEFFECT { 
  D3DSWAPEFFECT_DISCARD      = 1,
  D3DSWAPEFFECT_FLIP         = 2,
  D3DSWAPEFFECT_COPY         = 3,
  D3DSWAPEFFECT_OVERLAY      = 4,
  D3DSWAPEFFECT_FLIPEX       = 5,
  D3DSWAPEFFECT_FORCE_DWORD  = 0xFFFFFFFF
} D3DSWAPEFFECT, *LPD3DSWAPEFFECT;
```

## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ DISCARD**
</dt> <dd>

Quando uma cadeia de permuta é criada com um efeito de permuta de D3DSWAPEFFECT FLIP ou \_ D3DSWAPEFFECT COPY, o runtime garantirá que uma \_ operação [**IDirect3DDevice9::P resent**](/windows/desktop/api) não afetará o conteúdo de nenhum dos buffers de fundo. Infelizmente, atender a essa garantia pode envolver sobrecargas substanciais de processamento ou memória de vídeo, especialmente ao implementar semântica de invasões para uma cadeia de permuta em janelas ou semântica de cópia para uma cadeia de permuta de tela inteira. Um aplicativo pode usar o efeito de troca D3DSWAPEFFECT DISCARD para evitar essas sobrecargas e permitir que o driver de exibição selecione a técnica de apresentação mais eficiente para a cadeia \_ de permuta. Esse também é o único efeito de permuta que pode ser usado ao especificar um valor diferente de D3DMULTISAMPLE NONE para o membro \_ MultiSampleType [**de D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).

Como uma cadeia de permuta que usa D3DSWAPEFFECT FLIP, uma cadeia de permuta que usa D3DSWAPEFFECT DISCARD pode incluir mais de um buffer de retorno, qualquer um deles pode ser acessado usando \_ \_ [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) ou [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer). A cadeia de permuta é melhor prevista como uma fila na qual 0 sempre indexa o buffer de fundo que será exibido pela próxima operação Presente e da qual os buffers serão descartados quando eles foram exibidos.

Um aplicativo que usa esse efeito de permuta não pode fazer suposições sobre o conteúdo de um buffer de fundo descartado e, portanto, deve atualizar um buffer de fundo inteiro antes de invocar uma operação Present que o exibiria. Embora isso não seja imposto, a versão de depuração do runtime substituirá o conteúdo dos buffers de fundo descartados por dados aleatórios para permitir que os desenvolvedores verifiquem se seus aplicativos estão atualizando todas as superfícies do buffer de fundo corretamente.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ FLIP**
</dt> <dd>

A cadeia de permuta pode incluir vários buffers de fundo e é a melhor previu como uma fila circular que inclui o buffer frontal. Nessa fila, os buffers traseiros são sempre numerados sequencialmente de 0 a (n-1), em que n é o número de buffers de fundo, de modo que 0 denota o buffer apresentado menos recentemente. Quando presente é invocado, a fila é "girada" para que o buffer frontal se torne buffer (n-1), enquanto o buffer de fundo 0 se torna o novo buffer frontal.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**\_Cópia D3DSWAPEFFECT**
</dt> <dd>

Esse efeito de permuta pode ser especificado apenas para uma cadeia de permuta que contém um único buffer de fundo. Se a cadeia de permuta estiver em janela ou em tela inteira, o tempo de execução garantirá a semântica implícita por uma operação presente com base em cópia, ou seja, a operação deixa o conteúdo do buffer de fundo inalterado, em vez de substituí-lo pelo conteúdo do buffer frontal como uma operação presente com base em inversão.

Para uma cadeia de troca de tela inteira, o tempo de execução usa uma combinação de operações de inversão e operações de cópia, com suporte se necessário pelos buffers de fundo ocultos, para realizar a operação atual. Da mesma forma, a apresentação é sincronizada com o rerastreamento vertical do adaptador de vídeo e sua taxa é restrita pelo intervalo de apresentação escolhido. Uma cadeia de permuta especificada com o \_ sinalizador Immediate de intervalo de D3DPRESENT \_ é a única exceção. (Consulte a descrição do membro **PresentationIntervals** da estrutura de [**\_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) .) Nesse caso, uma operação atual copia o conteúdo do buffer de fundo diretamente para o buffer frontal sem aguardar o rerastreamento vertical.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**Sobreposição de D3DSWAPEFFECT \_**
</dt> <dd>

Use uma área dedicada de memória de vídeo que possa ser sobreposta na superfície primária. Nenhuma cópia é executada quando a sobreposição é exibida. A operação de sobreposição é executada no hardware, sem modificar os dados na superfície primária.

Diferenças entre o Direct3D 9 e o Direct3D 9Ex:

- D3DSWAPEFFECT OVERLAY só está disponível no Direct3D9Ex em execução no \_ Windows 7 (ou sistema operacional mais atual).

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**
</dt> <dd>

Designa quando um aplicativo está adotando o modo de in flip, durante o qual o quadro de um aplicativo é passado em vez de copiado para o DWM (Gerenciador de Janelas da Área de Trabalho) para composição quando o aplicativo está apresentando no modo em janelas. O modo de invasão permite que um aplicativo use com mais eficiência a largura de banda de memória, além de permitir que um aplicativo aproveite as estatísticas de tela inteira presentes. O modo de in flip não afeta o comportamento de tela inteira.

> [!Note]  
> Se você criar uma cadeia de permuta com D3DSWAPEFFECT FLIPEX, não poderá substituir o \_ **membro hDeviceWindow** da estrutura [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md) quando apresentar um novo quadro para exibição. Ou seja, você deve passar **NULL** para o parâmetro *hDestWindowOverride* [**de IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) para instruir o runtime a usar o **membro hDeviceWindow** **de D3DPRESENT \_ PARAMETERS** para a apresentação.

Diferenças entre o Direct3D 9 e o Direct3D 9Ex:

- D3DSWAPEFFECT FLIPEX só está disponível no Direct3D9Ex em execução no \_ Windows 7 (ou sistema operacional mais atual).

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O estado do buffer de fundo após uma chamada para Present é bem definido por cada um desses efeitos de permuta e se o dispositivo Direct3D foi criado com uma cadeia de permuta de tela inteira ou uma cadeia de permuta em janelas não tem efeito sobre esse estado. Em particular, o efeito de troca FLIP D3DSWAPEFFECT opera da mesma forma, seja em janelas ou em tela inteira, e o runtime do Direct3D garante isso criando \_ buffers extras. Como resultado, é recomendável que os aplicativos usem D3DSWAPEFFECT DISCARD sempre que possível para \_ evitar tais penalidades. Isso ocorre porque esse efeito de permuta será sempre o mais eficiente em termos de desempenho e consumo de memória.

Os aplicativos que usam D3DSWAPEFFECT \_ inverter ou D3DSWAPEFFECT \_ descartar não devem esperar que o destino de tela inteira funcione. Isso significa que o \_ estado de RENDERIZAÇÃO D3DRS DESTBLEND não funcionará conforme o esperado porque as cadeias de troca de tela inteira com esses efeitos de permuta não têm um formato de pixel explícito do ponto de vista do driver. O driver infere que eles devem assumir o formato de exibição, que não tem um canal alfa. Para contornar isso, execute as seguintes etapas:

-   Use a \_ cópia D3DSWAPEFFECT.
-   Verifique o \_ \_ \_ \_ sinalizador flip ou Discard D3DCAPS3 Alpha fullscreen \_ no membro Caps3 da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Esse sinalizador indica se o driver pode fazer a mesclagem alfa quando D3DSWAPEFFECT \_ flip ou D3DSWAPEFFECT \_ descartável é usado.
-   Os aplicativos que usam o efeito de permuta do modo flip (D3DSWAPEFFECT \_ FLIPEX) devem chamar [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) após uma alteração de região ou redimensionamento de janela para garantir que o conteúdo de exibição seja atualizado.

Uma janela invisível não pode receber eventos de modo de usuário; Além disso, uma janela invisível-fullscreen interfere na apresentação da janela de modo em janela de outra aplicativo. Portanto, cada aplicativo precisa garantir que uma janela de dispositivo esteja visível quando um SwapChain é apresentado no modo de tela inteira.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |

## <a name="see-also"></a>Confira também

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
