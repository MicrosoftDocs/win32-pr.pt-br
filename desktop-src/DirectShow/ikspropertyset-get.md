---
description: O método Get recupera uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: Método IKsPropertySet::Get (Ksproxy.h)
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
ms.openlocfilehash: fbfd44002270209c055b5a4003d9062a6821aeffb3ce71de7977fc20d0c64e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652238"
---
# <a name="ikspropertysetget-method"></a>Método IKsPropertySet::Get

O **método Get** recupera uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.

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

*guidPropSet* \[ Em\]
</dt> <dd>

O GUID do conjunto de propriedades .

</dd> <dt>

*dwPropID* \[ Em\]
</dt> <dd>

O identificador da propriedade dentro do conjunto de propriedades.

</dd> <dt>

*pInstanceData* \[ Em\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que contém dados de instância para a propriedade .

</dd> <dt>

*cbInstanceData* \[ Em\]
</dt> <dd>

O tamanho da matriz determinada em *pInstanceData*, em bytes.

</dd> <dt>

*pPropData* \[ out\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que recebe os dados da propriedade.

</dd> <dt>

*cbPropData* \[ Em\]
</dt> <dd>

O tamanho da matriz determinada em *pPropData,* em bytes.

</dd> <dt>

*pcbReturned* \[ out\]
</dt> <dd>

Recebe o número de bytes que o método copia para a *matriz pPropData.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                              | Descrição                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Êxito.<br/>                                                         |
| <dl> <dt>**E \_ PROP SET SEM \_ \_ SUPORTE**</dt> </dl> | Não há suporte para o conjunto de propriedades.<br/>                               |
| <dl> <dt>**E \_ \_ ID DE PROP \_ SEM SUPORTE**</dt> </dl>  | Não há suporte para a ID da propriedade para o conjunto de propriedades especificado.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Existe outra interface com esse nome no arquivo de header dsound.h. As duas interfaces não são compatíveis. A interface [IKsControl,](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) documentada no DDK do DirectShow, agora é a interface recomendada para passar conjuntos de propriedades entre drivers WDM e componentes de modo de usuário.

 

Para recuperar uma propriedade, aloce um buffer que esse método preencherá. Para determinar o tamanho do buffer necessário, **especifique NULL** para *pPropData* e zero (0) para *cbPropData.* Esse método retorna o tamanho do buffer necessário *em pcbReturned.*

Você deve incluir Ks.h antes de Ksproxy.h.

## <a name="examples"></a>Exemplos

O exemplo a seguir consulta um pin para sua categoria de pino, recuperando a **propriedade AMPROPERTY \_ PIN \_ CATEGORY.** (Consulte [Fixar Conjunto de Propriedades](pin-property-set.md).)


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
| Cabeçalho<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**IKsPropertySet Interface**](ikspropertyset.md)
</dt> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 
