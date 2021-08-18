---
description: Essa interface é usada para controlar a funcionalidade de animação, conectando conjuntos de animação com os quadros de transformação que estão sendo animados.
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: Interface ID3DXAnimationController (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d01bafe9a20e56741f7e8b7ec9828386883fbdc150632335a342240c0a64a858
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987806"
---
# <a name="id3dxanimationcontroller-interface"></a>Interface ID3DXAnimationController

Essa interface é usada para controlar a funcionalidade de animação, conectando conjuntos de animação com os quadros de transformação que estão sendo animados. A interface tem métodos para misturar várias animações e modificar parâmetros de mesclagem ao longo do tempo para habilitar transições suaves e outros efeitos.

## <a name="members"></a>Membros

A interface **ID3DXAnimationController** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXAnimationController** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXAnimationController** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)                             | Anima a malha e avança o tempo de animação global em um valor especificado.<br/>                                                              |
| [**CloneAnimationController**](id3dxanimationcontroller--cloneanimationcontroller.md)   | Clones ou cópias, um controlador de animação.<br/>                                                                                                  |
| [**GetAnimationSet**](id3dxanimationcontroller--getanimationset.md)                     | Obtém um conjunto de animação.<br/>                                                                                                                       |
| [**GetAnimationSetByName**](id3dxanimationcontroller--getanimationsetbyname.md)         | Obtém um conjunto de animação, considerando seu nome.<br/>                                                                                                       |
| [**GetCurrentPriorityBlend**](id3dxanimationcontroller--getcurrentpriorityblend.md)     | Retorna um alça de evento para um evento de combinação de prioridade que está em execução no momento.<br/>                                                                 |
| [**GetCurrentTrackEvent**](id3dxanimationcontroller--getcurrenttrackevent.md)           | Retorna um alça de evento para o evento em execução no momento na faixa de animação especificada.<br/>                                                     |
| [**GetEventDesc**](id3dxanimationcontroller--geteventdesc.md)                           | Obtém uma descrição de um evento de animação especificado.<br/>                                                                                           |
| [**GetMaxNumAnimationOutputs**](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | Obter o número máximo de saídas de animação que o controlador de animação pode dar suporte.<br/>                                                            |
| [**GetMaxNumAnimationSets**](id3dxanimationcontroller--getmaxnumanimationsets.md)       | Obtém o número máximo de conjuntos de animação que o controlador de animação pode dar suporte.<br/>                                                              |
| [**GetMaxNumEvents**](id3dxanimationcontroller--getmaxnumevents.md)                     | Obtém o número máximo de eventos que o controlador de animação pode dar suporte.<br/>                                                                      |
| [**GetMaxNumTracks**](id3dxanimationcontroller--getmaxnumtracks.md)                     | Obtém o número máximo de faixas no controlador de animação.<br/>                                                                               |
| [**GetNumAnimationSets**](id3dxanimationcontroller--getnumanimationsets.md)             | Retorna o número de conjuntos de animação atualmente registrados no controlador de animação.<br/>                                                       |
| [**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)                   | Obtém o peso de mesclagem de prioridade atual usado pelo controlador de animação.<br/>                                                                  |
| [**Gettime**](id3dxanimationcontroller--gettime.md)                                     | Obtém o tempo de animação global.<br/>                                                                                                              |
| [**GetTrackAnimationSet**](id3dxanimationcontroller--gettrackanimationset.md)           | Obtém o conjunto de animação para a faixa determinada.<br/>                                                                                                  |
| [**GetTrackDesc**](id3dxanimationcontroller--gettrackdesc.md)                           | Obtém a descrição da faixa.<br/>                                                                                                                  |
| [**GetUpcomingPriorityBlend**](id3dxanimationcontroller--getupcomingpriorityblend.md)   | Retorna um alça de evento para o próximo evento de combinação de prioridade agendado para ocorrer após um evento especificado.<br/>                                         |
| [**GetUpcomingTrackEvent**](id3dxanimationcontroller--getupcomingtrackevent.md)         | Retorna um alça de evento para o próximo evento agendado para ocorrer após um evento especificado em uma faixa de animação.<br/>                                  |
| [**KeyPriorityBlend**](id3dxanimationcontroller--keypriorityblend.md)                   | Define a combinação de chaves de evento para a faixa de animação especificada.<br/>                                                                                  |
| [**KeyTrackEnable**](id3dxanimationcontroller--keytrackenable.md)                       | Define uma chave de evento que habilita ou desabilita uma faixa de animação.<br/>                                                                               |
| [**KeyTrackPosition**](id3dxanimationcontroller--keytrackposition.md)                   | Define uma chave de evento que altera a hora local de uma faixa de animação.<br/>                                                                         |
| [**KeyTrackSpeed**](id3dxanimationcontroller--keytrackspeed.md)                         | Define uma chave de evento que altera a taxa de reprodução de uma faixa de animação.<br/>                                                                       |
| [**KeyTrackWeight**](id3dxanimationcontroller--keytrackweight.md)                       | Define uma chave de evento que altera o peso de uma faixa de animação. O peso é usado como um multiplicador ao combinar várias faixas juntas.<br/> |
| [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)     | Adiciona uma saída de animação ao controlador de animação e registra ponteiros para transformações de escala, rotação e tradução (SRT).<br/>          |
| [**RegisterAnimationSet**](id3dxanimationcontroller--registeranimationset.md)           | Adiciona um conjunto de animação ao controlador de animação.<br/>                                                                                           |
| [**ResetTime**](id3dxanimationcontroller--resettime.md)                                 | Redefine o tempo de animação global como zero. Todos os eventos pendentes manterão suas agendas originais, mas no novo período.<br/>                 |
| [**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)                   | Define o peso de mesclagem de prioridade usado pelo controlador de animação.<br/>                                                                          |
| [**SetTrackAnimationSet**](id3dxanimationcontroller--settrackanimationset.md)           | Aplica o conjunto de animação à faixa especificada.<br/>                                                                                            |
| [**SetTrackDesc**](id3dxanimationcontroller--settrackdesc.md)                           | Define a descrição da faixa.<br/>                                                                                                                  |
| [**SetTrackEnable**](id3dxanimationcontroller--settrackenable.md)                       | Habilita ou desabilita uma faixa no controlador de animação.<br/>                                                                                     |
| [**SetTrackPosition**](id3dxanimationcontroller--settrackposition.md)                   | Define a faixa para o tempo de animação local especificado.<br/>                                                                                        |
| [**SetTrackPriority**](id3dxanimationcontroller--settrackpriority.md)                   | Define o peso da combinação de prioridade para a faixa de animação especificada.<br/>                                                                         |
| [**SetTrackSpeed**](id3dxanimationcontroller--settrackspeed.md)                         | Define a velocidade da faixa. A velocidade da faixa é semelhante a um multiplicador usado para acelerar ou reduzir a velocidade da reprodução da faixa.<br/>            |
| [**SetTrackWeight**](id3dxanimationcontroller--settrackweight.md)                       | Define o peso da faixa. O peso é usado para determinar como combinar várias faixas.<br/>                                                |
| [**UnkeyAllPriorityBlends**](id3dxanimationcontroller--unkeyallpriorityblends.md)       | Remove todos os eventos de combinação de prioridade agendada do controlador de animação.<br/>                                                                   |
| [**UnkeyAllTrackEvents**](id3dxanimationcontroller--unkeyalltrackevents.md)             | Remove todos os eventos de uma faixa de animação especificada.<br/>                                                                                         |
| [**UnkeyEvent**](id3dxanimationcontroller--unkeyevent.md)                               | Remove um evento especificado de uma faixa de animação, impedindo a execução do evento.<br/>                                                    |
| [**UnregisterAnimationSet**](id3dxanimationcontroller--unregisteranimationset.md)       | Remove um conjunto de animação do controlador de animação.<br/>                                                                                      |
| [**Validateevent**](id3dxanimationcontroller--validateevent.md)                         | Verifica se um alça de evento especificado é válido e se o evento de animação ainda não foi concluído.<br/>                                              |



 

## <a name="remarks"></a>Comentários

Crie um objeto de controlador de animação [**com D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md).

O tipo LPD3DXANIMATIONCONTROLLER é definido como um ponteiro para a interface **ID3DXAnimationController.**


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



O tipo D3DXEVENTHANDLE é definido como um identificador de evento para eventos do controlador de animação.


```
typedef DWORD D3DXEVENTHANDLE;
```



O tipo LPD3DXEVENTHANDLE é definido como um ponteiro para um identificador de evento para eventos do controlador de animação.


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
