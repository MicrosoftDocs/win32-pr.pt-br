---
title: Network. taxa de bits
description: A propriedade taxa de bits recupera a taxa de bit atual que está sendo recebida.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Rede. taxa de bits Windows Media Player
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797612"
---
# <a name="networkbitrate"></a>Network. taxa de bits

A **Propriedade taxa de bits recupera** a taxa de bit atual que está sendo recebida.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **taxa de bits**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Esse valor é uma combinação das taxas de bits dos fluxos de áudio e vídeo atuais.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. taxa **de bits para exibir** a tarifa de bit de mídia atual. As informações são exibidas em uma DIV HTML criada com ID = "BR". O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

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

 

 





