---
title: Settings. Rate
description: A propriedade Rate especifica ou recupera a taxa de reprodução atual da mídia de vídeo.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Settings. Rate Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748108"
---
# <a name="settingsrate"></a>Settings. Rate

A propriedade **Rate** especifica ou recupera a taxa de reprodução atual da mídia de vídeo.

## <a name="syntax"></a>Syntax

Player. Settings. Rate

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** de leitura/gravação (**duplo**) com um valor padrão de 1,0.

## <a name="remarks"></a>Comentários

Essa propriedade atua como um valor de multiplicador que permite que você reproduza um clipe em uma taxa mais rápida ou mais lenta. O valor padrão de 1,0 indica a velocidade de criação. Observe que uma faixa de áudio torna-se difícil de entender em taxas menores que 0,5 ou superiores a 1,5. Uma taxa de reprodução de 2 equivale a duas vezes a velocidade de reprodução normal.

O Windows Media Player tentará usar o mais eficiente de quatro modos de reprodução diferentes. Esses modos são reprodução de vídeo suave com densidade de áudio mantida, reprodução de vídeo suave com densidade de áudio não mantida, reprodução de vídeo suave sem áudio e reprodução de vídeo com quadro-chave sem áudio. O modo escolhido pelo player depende de vários fatores, incluindo tipo de arquivo e local, sistema operacional, rede e servidor.

Outras considerações também se aplicam, dependendo do tipo de mídia:

-   Arquivos WMV (Windows Media Format) e ASF: os valores ideais para essa propriedade são de 1 a 10 ou de 1 a 10 para reprodução reversa. Os valores de 0,5 a 1,0 ou de-0,5 a-1,0 também podem funcionar bem em casos em que a densidade de áudio pode ser mantida, por exemplo, ao reproduzir arquivos localizados no computador local. Valores com uma magnitude absoluta maior que 10 são permitidos, mas não são muito significativos.
-   Outros tipos de mídia de vídeo: essa propriedade pode variar de 0 a 9. Valores negativos não são permitidos. Valores menores que 1 representam movimento lento. Os valores acima de 9 são permitidos, mas não são muito significativos.

Os *controles*. o método **Fastforward** altera o valor de **Rate** para 5,0, enquanto os *controles*. o método **fastReverse** altera a **taxa** para 5,0.

A taxa de reprodução de alguns tipos de mídia não pode ser alterada. Use as *configurações*. método **IsAvailable** para determinar se essa propriedade pode ser especificada para um item de mídia específico.

**Windows Media Player 10 Mobile**: essa propriedade só aceita ou retorna valores de-5,0, 1,0 ou 5,0.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento HTML SELECT que permite ao usuário alterar a velocidade de reprodução da mídia atual. As opções SELECT oferecem velocidade normal, meia velocidade e taxas de reprodução de velocidade dupla. O objeto de **jogador** foi criado com ID = "Player".


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. fastReverse**](controls-fastreverse.md)
</dt> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> <dt>

[**Settings. IsAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





