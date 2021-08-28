---
title: Controls.currentPositionTimecode
description: A propriedade currentPositionTimecode especifica ou recupera a posição atual no item de mídia atual usando um formato de código de hora. Atualmente, essa propriedade dá suporte ao código de hora SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Controls.currentPositionTimecode Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd0dcdf4c5337cf8dc447452ce9667c261a9c7ea4b11f98753a294bca20c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736536"
---
# <a name="controlscurrentpositiontimecode"></a>Controls.currentPositionTimecode

A **propriedade currentPositionTimecode** especifica ou recupera a posição atual no item de mídia atual usando um formato de código de hora. Atualmente, essa propriedade dá suporte ao código de hora SMPTE.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

O código de hora SMPTE fornece uma maneira padrão de identificar um quadro de vídeo individual, que é útil para sincronizar a reprodução. Se um arquivo de mídia digital for compatível com o código de tempo SMPTE, Windows Media Player poderá recuperar as informações de posição do código de hora atual ou buscar um quadro de vídeo identificado por um código de tempo específico **String**.

O código de tempo SMPTE identifica um quadro específico pelo número de horas, minutos, segundos e quadros que o separam de um quadro de referência específico, o quadro designado como hora zero. Normalmente, o período zero é o início do arquivo e um valor de código de tempo SMPTE específico representa o tempo decorrido desde o início do arquivo.

O código de hora **String** está no intervalo \[ *de formato* \] *hh*:*mm*:*ss*.*ff* em \[ *que range* \] representa o intervalo, *hh* representa horas, *mm* representa minutos, *ss* representa segundos e *ff* representa quadros. Ao especificar um valor usando **currentPositionTimecode**, você deve incluir todos os oito dígitos usando zeros como espaço reservados.

O \[ *especificador* de intervalo corresponde ao membro wRange da estrutura Windows dados de EXTENSÃO \] **DE \_ TIMECODE \_ \_ DO WMT de** formato de mídia.  Para obter mais informações sobre intervalos de código de tempo, consulte o SDK Windows Formato de Mídia.

A especificação e a recuperação **de currentPositionTimecode** só têm suporte para arquivos que contêm informações de código de hora SMPTE.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir especifica **currentPositionTimecode** como 1 hora, zero minutos, 30 segundos e 5 quadros. O **objeto** Player foi criado com ID = "Player".


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 





