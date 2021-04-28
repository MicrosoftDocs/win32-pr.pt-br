---
description: Função de proxy de função IWICBitmapFrameDecode_GetColorContexts_Proxy para o método GetColorContexts.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: Função IWICBitmapFrameDecode_GetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 99fb6caa9b9e654be0adc1235cad0e79a7fa1ef3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100574"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a>\_Função de \_ proxy GetColorContexts IWICBitmapFrameDecode

Função de proxy para o método [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***

Ponteiro para este objeto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .

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

Um ponteiro que recebe um ponteiro para os objetos [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) .

</dd> <dt>

*pcActualCount* \[ fora\]
</dt> <dd>

Tipo: **uint \***

Um ponteiro que recebe o número de contextos de cor contidos no quadro da imagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




