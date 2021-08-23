---
description: O método \_ put CurrentStream especifica o número de fluxo para o detector de mídia usar.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: Método IMediaDet::p ut_CurrentStream (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ba8b9cfe7cf898e9645d0f1caf8ef789bb45967bfc268f08555a5bdea53c4127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952595"
---
# <a name="imediadetput_currentstream-method"></a>Método IMediaDet::p ut \_ CurrentStream

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_CurrentStream` método especifica o número de fluxo para o detector de mídia usar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ Em\]
</dt> <dd>

Número do fluxo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Antes de chamar esse método, chame [**IMediaDet::p nome \_ do arquivo**](imediadet-put-filename.md) para definir o nome do arquivo. Chame [**IMediaDet::get \_ OutputStreams**](imediadet-get-outputstreams.md) para determinar o número de fluxos contidos no arquivo de origem.

Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG. Para obter mais informações, [**consulte IMediaDet::EnterBitmapGrabMode.**](imediadet-enterbitmapgrabmode.md)

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaDet Interface**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




