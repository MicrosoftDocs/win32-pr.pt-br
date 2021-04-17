---
description: O \_ método Get OutputStreams recupera o número de fluxos de áudio e vídeo contidos na origem da mídia. Quaisquer outros tipos de fluxo, como fluxos de dados, são ignorados.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'Método IMediaDet:: get_OutputStreams (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779523"
---
# <a name="imediadetget_outputstreams-method"></a>Método IMediaDet:: get \_ OutputStreams

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_OutputStreams` método recupera o número de fluxos de áudio e vídeo contidos na origem da mídia. Quaisquer outros tipos de fluxo, como fluxos de dados, são ignorados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe o número de fluxos de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Antes de chamar esse método, chame [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) para definir o nome do arquivo. Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG. Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




