---
title: Método ITfContextRenderingMarkup GetRenderingMarkup
description: O método ITfContextRenderingMarkup GetRenderingMarkup recupera um enumerador das marcações de renderização para o intervalo determinado.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Método GetRenderingMarkup Estrutura de Serviços de Texto
- Método GetRenderingMarkup Estrutura de Serviços de Texto interface , ITfContextRenderingMarkup
- Interface ITfContextRenderingMarkup Estrutura de Serviços de Texto , método GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a94c8a7cce8673560cf01091b819def343213bfde578df6ce1e8850e2721723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476947"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>Método ITfContextRenderingMarkup::GetRenderingMarkup

O **método ITfContextRenderingMarkup::GetRenderingMarkup** recupera um enumerador das marcações de renderização para o intervalo determinado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ec* \[ Em\]
</dt> <dd>

\[em \] Um cookie de edição somente leitura para acessar o contexto.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

\[Em\]



| Valor                                                                                                                                                                                         | Significado                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**PROPRIEDADE TF \_ GRM \_ \_ INCLUDE**</dt> </dl> | Se esse bit for 1, o enumerador incluirá a propriedade GUID \_ PROP \_ ATTRIBUTE.<br/> |



 

</dd> <dt>

*pRangeCover* \[ Em\]
</dt> <dd>

\[em \] Um ponteiro para uma interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) do intervalo para enumerar as marcações de renderização.

</dd> <dt>

*ppEnum* \[ out\]
</dt> <dd>

\[out \] Um ponteiro para recuperar o ponteiro da interface [IEnumTfRenderingMarkup.](/windows/desktop/TSF/ienumtfrenderingmarkup)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                | Descrição                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Esse método não está atualmente nos arquivos de header públicos. Para usar essa API, você deve compilar MIDL o [protótipo](prototypes.md).

 

 

