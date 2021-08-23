---
title: Propriedade IWMPControls3 currentPositionTimecode
description: A propriedade currentPositionTimecode obtém ou define a posição atual no item de mídia atual usando um formato de código de hora. Atualmente, essa propriedade dá suporte ao código de hora SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- propriedade currentPositionTimecode Windows Media Player
- propriedade currentPositionTimecode Windows Media Player , interface IWMPControls3
- Interface IWMPControls3 Windows Media Player , propriedade currentPositionTimecode
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c00c166050f4f3a3bc05861fa92d4fb66efcfa139e726c7cc799e21623fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760916"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>Propriedade IWMPControls3::currentPositionTimecode

A **propriedade currentPositionTimecode** obtém ou define a posição atual no item de mídia atual usando um formato de código de hora. Atualmente, essa propriedade dá suporte ao código de hora SMPTE.

## <a name="syntax"></a>Syntax


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System.String que** é o código de tempo SMPTE.

## <a name="remarks"></a>Comentários

O código de hora SMPTE fornece uma maneira padrão de identificar um quadro de vídeo individual, que é útil para sincronizar a reprodução. Se um arquivo de mídia digital dá suporte ao código de tempo SMPTE, Windows Media Player pode recuperar as informações de posição do código de hora atual ou buscar um quadro de vídeo identificado por um código de hora específico.

O código de tempo SMPTE identifica um quadro específico pelo número de horas, minutos, segundos e quadros que o separam de um quadro de referência específico, o quadro designado como hora zero. Normalmente, o período zero é o início do arquivo e um valor de código de tempo SMPTE específico representa o tempo decorrido desde o início do arquivo.

O código de hora está no intervalo \[ *de* \] *formato hh*:*mm*:*ss*.*ff* em \[ *que range* \] representa o intervalo, hh representa horas, *mm* representa minutos, *ss* representa segundos e *ff* representa quadros. Ao definir um valor para **currentPositionTimecode,** você deve incluir todos os oito dígitos, usando zeros como espaço reservado.

\[*intervalo* \] corresponde ao membro **wRange** da estrutura Windows dados de EXTENSÃO DE **TIMECODE DO WMT de formato \_ \_ \_ de** mídia. Para obter mais informações sobre intervalos de código de tempo, consulte o SDK Windows Formato de Mídia.

A configuração e **a adoção de currentPositionTimecode** só têm suporte para arquivos que contêm informações de código de hora SMPTE.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir especifica **currentPositionTimecode** como 1 hora, zero minutos, 30 segundos e 5 quadros. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





