---
description: O método Get recupera uma propriedade identificada por um GUID do conjunto de propriedades e uma ID de propriedade.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'Método IKsPropertySet:: Get (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456635"
---
# <a name="ikspropertysetget-method"></a>Método IKsPropertySet:: Get

O método **Get** recupera uma propriedade identificada por um GUID do conjunto de propriedades e uma ID de propriedade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*guidPropSet* \[ no\]
</dt> <dd>

O GUID do conjunto de propriedades.

</dd> <dt>

*dwPropId* \[ no\]
</dt> <dd>

O identificador da propriedade dentro do conjunto de propriedades.

</dd> <dt>

*pInstanceData* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que contém dados de instância para a propriedade.

</dd> <dt>

*cbInstanceData* \[ no\]
</dt> <dd>

O tamanho da matriz fornecida em *pInstanceData*, em bytes.

</dd> <dt>

*pPropData* \[ fora\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que recebe os dados de propriedade.

</dd> <dt>

*cbPropData* \[ no\]
</dt> <dd>

O tamanho da matriz fornecida em *pPropData*, em bytes.

</dd> <dt>

*pcbReturned* \[ fora\]
</dt> <dd>

Recebe o número de bytes que o método copia para a matriz *pPropData* .

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
> Outra interface com esse nome existe no arquivo de cabeçalho dsound. h. As duas interfaces não são compatíveis. A interface [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário.

 

Para recuperar uma propriedade, aloque um buffer que esse método irá preencher. Para determinar o tamanho de buffer necessário, especifique **NULL** para *pPropData* e zero (0) para *cbPropData*. Esse método retorna o tamanho de buffer necessário em *pcbReturned*.

Você deve incluir KS. h antes de ksproxy. h.

## <a name="examples"></a>Exemplos

O exemplo a seguir consulta um PIN para sua categoria de PIN, recuperando a propriedade de **\_ \_ categoria AMPROPERTY PIN** . (Consulte [PIN conjunto de propriedades](pin-property-set.md).)


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



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

 

 
