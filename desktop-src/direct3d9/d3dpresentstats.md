---
description: Descreve as estatísticas de SwapChain relacionadas a chamadas PresentEx.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Estrutura D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173054"
---
# <a name="d3dpresentstats-structure"></a>Estrutura D3DPRESENTSTATS

Descreve as estatísticas de SwapChain relacionadas a chamadas [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a>Membros

<dl> <dt>

**PresentCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Contagem em execução de chamadas presentes bem-sucedidas feitas por um dispositivo de vídeo que está sendo disponibilizado para a tela. Esse parâmetro é realmente a ID atual da última chamada presente e não é necessariamente o número total de chamadas de API presentes.

</dd> <dt>

**PresentRefreshCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

A contagem de vblank em que a última apresentação foi exibida na tela, a contagem de vblank é incrementada uma vez a cada intervalo de vblank.

</dd> <dt>

**SyncRefreshCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

A contagem de vblank quando o Agendador último amostra a hora da máquina chamando QueryPerformanceCounter.

</dd> <dt>

**SyncQPCTime**
</dt> <dd>

Tipo: **[ **\_ inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

A última hora da máquina de amostra do Agendador, obtida com a chamada de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> <dt>

**SyncGPUTime**
</dt> <dd>

Tipo: **[ **\_ inteiro grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando um aplicativo 9Ex adota o modo invertido presente (D3DSWAPEFFECT \_ FLIPEX), os aplicativos podem detectar o descarte de quadros chamando GetPresentStatistics em qualquer ponto no tempo. Na verdade, eles podem fazer o seguinte.

1.  Renderizar para o buffer de fundo
2.  Chamada presente
3.  Chamar GetPresentStats e armazenar a estrutura D3DPRESENTSTATS resultante
4.  Renderizar o próximo quadro para o buffer de fundo
5.  Chamada presente
6.  Repita as etapas 4 e 5 1 ou mais vezes
7.  Chamar GetPresentStats e armazenar a estrutura D3DPRESENTSTATS resultante
8.  Compare os valores de PresentRefreshCount das duas estruturas D3DPRESENTSTATS armazenadas. O aplicativo pode calcular o PresentRefreshCount correspondente de um parâmetro PresentCount específico com base nas suposições do incremento de PresentRefreshCount e PresentCount atribuição de quadro apresenta. Se o PresentRefreshCount da última amostra não corresponder ao PresentCount (ou seja, se o PresentRefreshCount tiver sido incrementado, mas PresentCount não tiver, havia um descarte de quadros.)

Os aplicativos podem determinar se um quadro foi descartado por amostragem de duas instâncias de PresentCount e GetPresentStats (chamando a API GetPresentStats em dois pontos no tempo). Por exemplo, um aplicativo de mídia que está apresentando na mesma taxa que a taxa de atualização do monitor (por exemplo, a taxa de atualização do monitor é de 60, o aplicativo apresenta um quadro a cada 1/60 segundos) quer apresentar os quadros A, B, C, D, E, cada um correspondendo às IDs presentes (PresentCount) 1, 2, 3, 7, 8.

O código do aplicativo é semelhante à sequência a seguir.

1.  Renderizar o quadro a para o buffer de fundo
2.  Chamada presente, PresentCount = 1
3.  Chamar GetPresentStats e armazenar a estrutura D3DPRESENTSTATS resultante
4.  Renderizar os próximos 4 quadros, B, C, D, E, respectivamente
5.  Chamada presente 4 vezes, PresentCounts = 2, 3, 7, 8, respectivamente
6.  Chamar GetPresentStats e armazenar a estrutura D3DPRESENTSTATS resultante
7.  Compare os valores de PresentRefreshCount das duas estruturas D3DPRESENTSTATS armazenadas. Se a diferença for 2, ou seja, 2 intervalos de vblank decorridos entre as duas chamadas de API GetPresentStats, o último quadro apresentado deverá ser o quadro C. Como o aplicativo apresenta uma vez vblank intervalo (a taxa de atualização do monitor), o tempo decorrido entre quando o quadro A é apresentado e quando o quadro C é apresentado deve ser 2 vblanks.
8.  Compare os valores de PresentCount das duas estruturas D3DPRESENTSTATS armazenadas. Se o primeiro PresentCount for 1 (correspondente ao quadro A) e o segundo PresentCount for 3 (correspondente ao quadro C), nenhum quadro foi Descartado. Se o segundo PresentCount for 3, que corresponde ao quadro D, o aplicativo saberá que um quadro foi Descartado.

Observe que GetPresentStatistics será processado depois que for chamado, independentemente do estado de chamadas PresentEx do modo FLIPEX.

**Windows Vista:** As chamadas presentes serão enfileiradas e, em seguida, processadas antes que a chamada a GetPresentStats seja processada.

Quando um aplicativo detecta que a apresentação de determinados quadros está atrás, ele pode ignorar esses quadros e corrigir a apresentação para sincronizar novamente com o vblank. Para fazer isso, um aplicativo pode simplesmente não renderizar os quadros atrasados e iniciar a renderização com o próximo quadro correto na fila. No entanto, se um aplicativo já tiver iniciado o processamento de quadros atrasados, ele poderá usar um novo parâmetro presente em D3D9Ex chamado D3DPRESENT \_ FORCEIMMEDIATE. O sinalizador será passado nos parâmetros da chamada de API atual e indicará o tempo de execução que o quadro será processado imediatamente no próximo intervalo de vblank, efetivamente não visível na tela. Aqui está o exemplo de uso do aplicativo após a última etapa no exemplo anterior.

1.  Renderizar o próximo quadro para o buffer de fundo
2.  Descobrir de PresentRefreshCount que o próximo quadro já está atrasado
3.  Definir intervalo atual para D3DPRESENT \_ FORCEIMMEDIATE
4.  Chamada presente no próximo quadro

Os aplicativos podem sincronizar fluxos de áudio e vídeo da mesma maneira porque o comportamento de GetPresentStatistics não é alterado nesse cenário.

O modo flip D3D9Ex fornece informações de estatísticas de quadro para aplicativos em janelas e aplicativos de tela inteira.

**Windows Vista:** Use as APIs do DWM para recuperar as estatísticas presentes.

Quando Gerenciador de Janelas da Área de Trabalho estiver desativada, o modo em janela do 9Ex Applications usando o modo flip receberá informações estatísticas atuais de precisão limitada.

* * Windows Vista: * *

Se um aplicativo não for rápido o suficiente para acompanhar a taxa de atualização do monitor, possivelmente devido ao hardware lento ou à falta de recursos do sistema, ele poderá enfrentar uma falha de gráficos. Uma falha é uma chamada intermitência Visual. Se um monitor estiver configurado para ser atualizado em 60 Hz, e o aplicativo só puder gerenciar 30 fps, metade dos quadros terá problemas.

Os aplicativos podem detectar uma falha mantendo o controle do SynchRefreshCount. Por exemplo, um aplicativo pode executar a seguinte sequência de ações.

1.  Renderizar para o buffer de fundo.
2.  Chamada presente.
3.  Chame GetPresentStats e armazene a estrutura D3DPRESENTSTATS resultante.
4.  Renderizar o próximo quadro para o buffer de fundo.
5.  Chamada presente.
6.  Chame GetPresentStats e armazene a estrutura D3DPRESENTSTATS resultante.
7.  Compare os valores de SyncRefreshCount das duas estruturas D3DPRESENTSTATS armazenadas. Se a diferença for maior que um, um quadro foi ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
