---
description: Função de proxy para o método GetColorContexts.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: Função IWICBitmapDecoder_GetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 737ad4b8bbb0014a04129d3a264cecaed4b5fe8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765275"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a>\_Função de \_ proxy IWICBitmapDecoder GetColorContexts

Função de proxy para o método [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _

Ponteiro para este objeto [_ *IWICBitmapDecoder* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*conta* \[ no\]
</dt> <dd>

Tipo: **uint**

O número de contextos de cor a serem recuperados.

Esse valor deve ser o tamanho ou menor que o tamanho disponível para *ppIColorContexts*.

</dd> <dt>

*ppIColorContexts* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***

Um ponteiro que recebe um ponteiro para o [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).

</dd> <dt>

*pcActualCount* \[ fora\]
</dt> <dd>

Tipo: **uint \** _

Um ponteiro que recebe o número de contextos de cor contidos na imagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




