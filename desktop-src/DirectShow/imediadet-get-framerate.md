---
description: O \_ método Get de taxa de quadros recupera a taxa de quadros do fluxo atual. O fluxo deve ser um fluxo de vídeo.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'Método IMediaDet:: get_FrameRate (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779524"
---
# <a name="imediadetget_framerate-method"></a>Método IMediaDet:: obter a \_ taxa de quadros

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_FrameRate` método recupera a taxa de quadros do fluxo atual. O fluxo deve ser um fluxo de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe a taxa de quadros, em quadros por segundo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                             | Descrição                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>                 | O cabeçalho de formato de vídeo não especifica uma taxa de quadros.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argumento inválido.<br/>                                  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>               | Argumento de ponteiro **nulo** .<br/>                         |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de mídia inválido.<br/>                                |



 

## <a name="remarks"></a>Comentários

Esse método não pode recuperar a taxa de quadros de um arquivo ASF.

Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG. Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

 

 




