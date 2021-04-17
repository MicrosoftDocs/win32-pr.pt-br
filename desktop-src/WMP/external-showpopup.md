---
title: Método external. ShowPopup
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. ShowPopup
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- método de pop-up Windows Media Player
- método de pop-up Windows Media Player, classe externa
- Classe externa Windows Media Player, método ShowPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783602"
---
# <a name="externalshowpopup-method"></a>Método external. ShowPopup

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **ShowPopup** instrui o Windows Media Player a exibir uma página da Web pop-up; ou seja, uma página da Web que aparece em uma janela separada.

## <a name="syntax"></a>Sintaxe


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PopupIndex* \[ no\]
</dt> <dd>

**Número** (**longo**) que especifica o índice da página da Web pop-up.

</dd> <dt>

*Parâmetros* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que o Windows Media Player acrescenta à URL da página da Web.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O índice pop-up não é interpretado pelo Windows Media Player. Os índices que identificam páginas da Web pop-up são criados pela loja online e têm significado apenas para a loja online.

As etapas a seguir mostram como o Windows Media Player usa os parâmetros do método **ShowPopup** para criar uma URL para a janela pop-up.

1.  O script em uma página de descoberta chama **Popup**, passando um inteiro em *PopupIndex* e uma cadeia de caracteres em *parâmetros*.

2.  O Windows Media Player passa o índice para [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para recuperar a URL da página da Web a ser exibida.

3.  O Windows Media Player acrescenta *parâmetros* à URL como uma cadeia de caracteres de consulta. Por exemplo, se **GetItemInfo** retornar " https://www.Proseware.com/Pages/Popup1.htm " e os *parâmetros* forem iguais a "DlgX = 800&DlgY = 400&greeting = Hi", o Windows Media Player criará a seguinte URL:

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

Você pode usar *parâmetros* para especificar o tamanho da janela pop-up. Por exemplo, se você definir *parâmetros* como "DlgX = 800&DlgY = 400", a janela pop-up terá um tamanho de 800 pixels por 400 pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





