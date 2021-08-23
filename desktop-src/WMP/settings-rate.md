---
title: Configurações.rate
description: A propriedade rate especifica ou recupera a taxa de reprodução atual da mídia de vídeo.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Configurações.rate Windows Media Player
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
ms.openlocfilehash: 01936462593b8b27a8d45f2e3e4090b9cf242d79e1d9b1c2cda00c152bd41182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646396"
---
# <a name="settingsrate"></a>Configurações.rate

A **propriedade rate** especifica ou recupera a taxa de reprodução atual da mídia de vídeo.

## <a name="syntax"></a>Syntax

player.settings.rate

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um  número de leitura/gravação (**double**) com um valor padrão de 1,0.

## <a name="remarks"></a>Comentários

Essa propriedade atua como um valor multiplicador que permite reproduzir um clipe em uma taxa mais rápida ou mais lenta. O valor padrão de 1,0 indica a velocidade de autor. Observe que uma faixa de áudio torna-se difícil de entender em taxas inferiores a 0,5 ou superiores a 1,5. Uma taxa de reprodução de 2 equivale a duas vezes a velocidade de reprodução normal.

Windows Media Player tentará usar o mais eficaz de quatro modos de reprodução diferentes. Esses modos são reprodução de vídeo suave com tom de áudio mantido, reprodução de vídeo suave com tom de áudio não mantido, reprodução de vídeo suave sem áudio e reprodução de vídeo de keyframe sem áudio. O modo escolhido pelo Player depende de vários fatores, incluindo tipo de arquivo e local, sistema operacional, rede e servidor.

Outras considerações também se aplicam, dependendo do tipo de mídia:

-   Windows Formato de mídia (WMV) e arquivos ASF: os valores ideais para essa propriedade são de 1 a 10 ou de 1 a 10 para reprodução inversa. Os valores de 0,5 a 1,0 ou de -0,5 a -1.0 também podem funcionar bem em casos em que o tom de áudio pode ser mantido, por exemplo, ao tocar arquivos localizados no computador local. Valores com uma magnitude absoluta maior que 10 são permitidos, mas não são muito significativos.
-   Outros Tipos de Mídia de Vídeo: essa propriedade pode variar de 0 a 9. Valores negativos não são permitidos. Valores menores que 1 representam movimento lento. Valores acima de 9 são permitidos, mas não são muito significativos.

Os *controles*. **O método fastForward** altera o valor **da taxa** para 5,0, enquanto o *controla*. **O método fastReverse** altera **a taxa** para 5,0.

A taxa de reprodução de alguns tipos de mídia não pode ser alterada. Use o *Configurações*. **Método isAvailable** para determinar se essa propriedade pode ser especificada para um item de mídia específico.

**Windows Media Player 10 Mobile:** essa propriedade só aceita ou retorna valores de -5.0, 1.0 ou 5.0.

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento HTML SELECT que permite que o usuário altere a velocidade de reprodução da mídia atual. As opções SELECT oferecem velocidade normal, taxas de reprodução de meia velocidade e velocidade dupla. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controls.fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls.fastReverse**](controls-fastreverse.md)
</dt> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> <dt>

[**Configurações.isAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





