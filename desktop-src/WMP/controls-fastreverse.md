---
title: Método Controls. fastReverse
description: O método fastReverse inicia a verificação rápida do item de mídia na direção inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- Windows Media Player do método fastReverse
- método fastReverse Windows Media Player, classe Controls
- classe Controls Windows Media Player, método fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4643525f66102cbd7b017a4a48f1068489062ec0849f197f1f55df45fc6f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580272"
---
# <a name="controlsfastreverse-method"></a>Método Controls. fastReverse

O método **fastReverse** inicia a verificação rápida do item de mídia na direção inversa.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **fastReverse** examina o clipe de forma inversa em cinco vezes a velocidade normal, exibindo apenas os quadros-chave se for um arquivo de vídeo. invocar **fastReverse** altera o *Configurações*. **taxa** de propriedade para 5,0. se a **taxa** for alterada posteriormente, ou se a **opção reproduzir** ou **parar** for chamada, Windows Media Player interromperá a inversão rápida.

Se o item fizer parte de uma lista de reprodução, o **fastReverse** para no início da faixa atual. por exemplo, se track 3 estiver em **fastReverse**, quando o início do track 3 for atingido, Windows Media Player não vai para o track 2. A contagem de execuções não é incrementada ao chamar **fastReverse**.

Se você chamar **Fastforward** enquanto **fastReverse** estiver em vigor, **fastReverse** será interrompido e **Fastforward** será iniciado.

Esse método não funciona para transmissões ao vivo e certos tipos de mídia. Para determinar se você pode usar a inversão rápida em um clipe, chame **IsAvailable**("fastReverse").

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de botão HTML que usa **fastReverse** para iniciar a reprodução rápida do item de mídia. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. IsAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. Stop**](controls-stop.md)
</dt> <dt>

[**taxa de Configurações.**](settings-rate.md)
</dt> </dl>

 

 





