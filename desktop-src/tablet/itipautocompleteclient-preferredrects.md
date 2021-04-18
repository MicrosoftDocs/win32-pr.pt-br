---
description: Permite que o cliente sugira onde posicionar a lista de preenchimento automático para evitar sobreposição do painel de entrada.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: 'ITipAutocompleteClient: método referredRects de:P (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802085"
---
# <a name="itipautocompleteclientpreferredrects-method"></a>ITipAutocompleteClient: método referredRects de:P

Permite que o cliente sugira onde posicionar a lista de preenchimento automático para evitar sobreposição do painel de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*prcACList* \[ no\]
</dt> <dd>

Um retângulo, em coordenadas da tela, indicando o local preferido do provedor e o tamanho da interface de usuário da lista de preenchimento automático.

</dd> <dt>

*prcField* \[ no\]
</dt> <dd>

Um retângulo, em coordenadas da tela, indicando o local e o tamanho do campo focado.

</dd> <dt>

*prcModified* \[ fora\]
</dt> <dd>

Um retângulo com base no estado atual da TIP e o local e o tamanho da lista de preenchimento automático preferenciais especificados por *prcACList*.

</dd> <dt>

*pfShownAboveTip* \[ entrada, saída\]
</dt> <dd>

**True** se o retângulo modificado for mostrado acima da área de destino do painel de entrada de texto; caso contrário, **false**. Esse valor deve ser inicializado para a orientação preferida do provedor antes de o método ser chamado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                  | Descrição                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Chame o [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) para definir a janela de lista de preenchimento automático de pop-up antes de chamar o [**método ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md).<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>       | Ocorreu um erro não especificado.<br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Esse é o método que o provedor de preenchimento automático chama quando está prestes a mostrar a interface do usuário de preenchimento automático. O cliente modifica o retângulo preferencial do provedor especificado por *prcACList* por meio do argumento *prcModified* .

Chame o [**método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) para definir o identificador de janela de lista de preenchimento automático de pop-up antes de chamar **PreferredRects**. A falha em fazer isso causará um erro **E \_ INVALIDARG** ao chamar **PreferredRects**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| parâmetro<br/>                   | <dl> <dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**Método ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




