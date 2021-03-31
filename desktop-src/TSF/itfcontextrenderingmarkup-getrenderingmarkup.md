---
title: Método ITfContextRenderingMarkup GetRenderingMarkup
description: O método ITfContextRenderingMarkup GetRenderingMarkup recupera um enumerador das marcações de renderização para o intervalo especificado.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Estrutura de serviços de texto do método GetRenderingMarkup
- Método GetRenderingMarkup de estrutura de serviços de texto, interface ITfContextRenderingMarkup
- Estrutura de serviços de texto da interface ITfContextRenderingMarkup, método GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641413"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>Método ITfContextRenderingMarkup:: GetRenderingMarkup

O método **ITfContextRenderingMarkup:: GetRenderingMarkup** recupera um enumerador das marcações de renderização para o intervalo especificado.

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

*EC* \[ no\]
</dt> <dd>

\[em \] um cookie de edição somente leitura para acessar o contexto.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

\[Em\]



| Valor                                                                                                                                                                                         | Significado                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**Propriedade de inclusão de TF \_ GRM \_ \_**</dt> </dl> | Se esse bit for 1, o enumerador incluirá a \_ propriedade de atributo de prop de GUID \_ .<br/> |



 

</dd> <dt>

*pRangeCover* \[ no\]
</dt> <dd>

\[em \] um ponteiro para uma interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) do intervalo para enumerar as marcações de renderização.

</dd> <dt>

*ppEnum* \[ fora\]
</dt> <dd>

\[\]um ponteiro para recuperar o ponteiro de interface [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                | Descrição                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Esse método não está atualmente nos arquivos de cabeçalho públicos. Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.

 

 

