---
description: O método set define uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'Método IKsPropertySet:: Set (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370193"
---
# <a name="ikspropertysetset-method"></a>Método IKsPropertySet:: Set

O `Set` método define uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*guidPropSet* \[ no\]
</dt> <dd>

GUID do conjunto de propriedades.

</dd> <dt>

*dwPropId* \[ no\]
</dt> <dd>

Identificador da propriedade dentro do conjunto de propriedades.

</dd> <dt>

*pInstanceData* \[ no\]
</dt> <dd>

Ponteiro para um buffer que contém dados de instância para a propriedade.

</dd> <dt>

*cbInstanceData* \[ no\]
</dt> <dd>

Tamanho do buffer *pInstanceData* , em bytes.

</dd> <dt>

*pPropData* \[ no\]
</dt> <dd>

Ponteiro para um buffer que contém o valor da propriedade.

</dd> <dt>

*cbPropData* \[ no\]
</dt> <dd>

Sise do buffer *pPropData* , em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                              | Descrição                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Êxito.<br/>                                                         |
| <dl> <dt>**\_ \_ \_ não há suporte para o conjunto de propriedades E**</dt> </dl> | Não há suporte para o conjunto de propriedades.<br/>                               |
| <dl> <dt>**ID de prop. de E \_ \_ \_ sem suporte**</dt> </dl>  | A ID da propriedade não tem suporte para o conjunto de propriedades especificado.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Outra interface com esse nome existe no arquivo de cabeçalho dsound. h. As duas interfaces não são compatíveis. A interface **IKsControl** , documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário.

 

Você deve incluir KS. h antes de ksproxy. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**Interface IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 




