---
description: O método QuerySupported determina se um objeto dá suporte a um conjunto de propriedades especificado.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Método IKsPropertySet:: QuerySupported (KS. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 7c79e81171349e2c481535eeab212717de072b17778b052dac3fc377cea0e094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792316"
---
# <a name="ikspropertysetquerysupported-method"></a>Método IKsPropertySet:: QuerySupported

O `QuerySupported` método determina se um objeto dá suporte a um conjunto de propriedades especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
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

*pTypeSupport* \[ fora\]
</dt> <dd>

Ponteiro para um valor no qual armazenar sinalizadores indicando o suporte fornecido pelo driver. Os sinalizadores com suporte incluem o seguinte.



| Valor                    | Descrição                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| \_Get de suporte do KSPROPERTY \_ | Você pode recuperar a propriedade chamando o método [**IKsPropertySet:: Get**](ikspropertyset-get.md) . |
| \_conjunto de suporte do KSPROPERTY \_ | Você pode alterar a propriedade chamando [**IKsPropertySet:: Set**](ikspropertyset-set.md).              |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                              | Descrição                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Há suporte para a combinação de conjunto de propriedades e ID de propriedade especificados.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                | Não há suporte para o conjunto de propriedades.<br/>                                       |
| <dl> <dt>**ID de prop. de E \_ \_ \_ sem suporte**</dt> </dl>  | A ID da propriedade não tem suporte para o conjunto de propriedades especificado.<br/>         |
| <dl> <dt>**\_ \_ \_ não há suporte para o conjunto de propriedades E**</dt> </dl> | Não há suporte para o conjunto de propriedades.<br/>                                       |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Outra interface com esse nome existe no arquivo de cabeçalho dsound. h. As duas interfaces não são compatíveis. a interface **IKsControl** , documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário.

 

Você deve incluir KS. h antes de ksproxy. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                             |
| Cabeçalho<br/>                   | <dl> <dt>KS. h; </dt> <dt>Ksproxy. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**Interface IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 




