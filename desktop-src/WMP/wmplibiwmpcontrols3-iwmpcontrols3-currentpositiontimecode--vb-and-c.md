---
title: Propriedade IWMPControls3 currentPositionTimecode
description: A propriedade currentPositionTimecode Obtém ou define a posição atual no item de mídia atual usando um formato de código de tempo. Essa propriedade atualmente dá suporte ao código de tempo SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Propriedade currentPositionTimecode Windows Media Player
- Propriedade currentPositionTimecode Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, Propriedade currentPositionTimecode
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
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747687"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>Propriedade IWMPControls3:: currentPositionTimecode

A propriedade **currentPositionTimecode** Obtém ou define a posição atual no item de mídia atual usando um formato de código de tempo. Essa propriedade atualmente dá suporte ao código de tempo SMPTE.

## <a name="syntax"></a>Syntax


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é o código de tempo SMPTE.

## <a name="remarks"></a>Comentários

O código de tempo SMPTE fornece uma maneira padrão de identificar um quadro de vídeo individual, que é útil para sincronizar a reprodução. Se um arquivo de mídia digital oferecer suporte a código de hora SMPTE, o Windows Media Player poderá recuperar as informações de posição de código da hora atual ou buscar um quadro de vídeo identificado por um código de tempo específico.

O código de tempo SMPTE identifica um determinado quadro pelo número de horas, minutos, segundos e quadros que o separam de um quadro de referência específico o quadro designado como tempo zero. Geralmente, o quadro de tempo zero é o início do arquivo e um determinado valor de código de tempo SMPTE representa o tempo decorrido desde o início do arquivo.

O código de tempo está no intervalo de formato \[  \] *hh*:*mm*:*SS*.*FF* em que \[ *Range* \] representa o intervalo, hh representa horas, *mm* representa minutos, *SS* representa segundos e *FF* representa quadros. Ao definir um valor para **currentPositionTimecode**, você deve incluir todos os oito dígitos, usando zeros como espaços reservados.

\[*intervalo* \] de corresponde ao membro **wRange** da estrutura de **dados de extensão do \_ código \_ \_ de WMT** do formato de mídia do Windows. Para obter mais informações sobre intervalos de código de tempo, consulte o SDK do Windows Media Format.

Só há suporte para a configuração e obtenção de **currentPositionTimecode** para arquivos que contêm informações de código de tempo SMPTE.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir especifica **currentPositionTimecode** como 1 hora, zero minutos, 30 segundos e 5 quadros. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


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
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





