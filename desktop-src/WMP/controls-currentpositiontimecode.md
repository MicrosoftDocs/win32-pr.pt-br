---
title: Controls. currentPositionTimecode
description: A propriedade currentPositionTimecode especifica ou recupera a posição atual no item de mídia atual usando um formato de código de tempo. Essa propriedade atualmente dá suporte ao código de tempo SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Controls. currentPositionTimecode Windows Media Player
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
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796434"
---
# <a name="controlscurrentpositiontimecode"></a>Controls. currentPositionTimecode

A propriedade **currentPositionTimecode** especifica ou recupera a posição atual no item de mídia atual usando um formato de código de tempo. Essa propriedade atualmente dá suporte ao código de tempo SMPTE.

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

O código de tempo SMPTE fornece uma maneira padrão de identificar um quadro de vídeo individual, que é útil para sincronizar a reprodução. Se um arquivo de mídia digital der suporte a código de hora SMPTE, o Windows Media Player poderá recuperar as informações de posição do código de tempo atual ou buscar um quadro de vídeo identificado por uma **cadeia de caracteres** de código de tempo específica.

O código de tempo SMPTE identifica um determinado quadro pelo número de horas, minutos, segundos e quadros que o separam de um quadro de referência específico o quadro designado como tempo zero. Geralmente, o quadro de tempo zero é o início do arquivo e um determinado valor de código de tempo SMPTE representa o tempo decorrido desde o início do arquivo.

A cadeia de **caracteres** de código de tempo está no intervalo de formato \[  \] *hh*:*mm*:*SS*.*FF* em que \[ *Range* \] representa o intervalo, *hh* representa horas, *mm* representa minutos, *SS* representa segundos e *FF* representa quadros. Ao especificar um valor usando **currentPositionTimecode**, você deve incluir todos os oito dígitos usando zeros como espaços reservados.

O \[  \] especificador de intervalo corresponde ao membro **wRange** da estrutura de dados de extensão do código de WMT do formato de mídia do Windows. **\_ \_ \_** Para obter mais informações sobre intervalos de código de tempo, consulte o SDK do Windows Media Format.

Só há suporte para a especificação e recuperação de **currentPositionTimecode** para arquivos que contêm informações de código de tempo SMPTE.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir especifica **currentPositionTimecode** como 1 hora, zero minutos, 30 segundos e 5 quadros. O objeto de **jogador** foi criado com ID = "Player".


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> </dl>

 

 





