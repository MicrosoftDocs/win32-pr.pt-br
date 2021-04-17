---
title: Network. bufferingTime
description: A propriedade bufferingTime especifica ou recupera a quantidade de tempo em milissegundos alocada para armazenar em buffer os dados de entrada antes do início da execução.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Network. bufferingTime Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761069"
---
# <a name="networkbufferingtime"></a>Network. bufferingTime

A propriedade **bufferingTime** especifica ou recupera a quantidade de tempo em milissegundos alocada para armazenar em buffer os dados de entrada antes do início da execução.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **bufferingTime**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** de leitura/gravação (**longo**) que varia de zero a 60.000 com um valor padrão de 5.000.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **bufferingTime** para especificar o número de segundos alocados para armazenar em buffer os dados de entrada. As informações são recuperadas de um elemento de entrada de texto HTML criado com ID = "bufText". O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> </dl>

 

 





