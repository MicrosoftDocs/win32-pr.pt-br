---
description: O método SetRecompFormatFromSource define o formato de recompactação de vídeo usando o formato de compactação de um arquivo de origem.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'Método IAMTimelineGroup:: SetRecompFormatFromSource (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810227"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a>Método IAMTimelineGroup:: SetRecompFormatFromSource

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetRecompFormatFromSource` método define o formato de recompactação de vídeo usando o formato de compactação de um arquivo de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSource* 
</dt> <dd>

Ponteiro para a interface [**IAMTimelineSrc**](iamtimelinesrc.md) do objeto de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                             | Descrição                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                                                                                    |
| <dl> <dt>**E \_ sem \_ linha do tempo**</dt> </dl>          | O grupo não está dentro de uma linha do tempo.<br/>                                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memória insuficiente.<br/>                                                                        |
| <dl> <dt>**\_ponteiro E**</dt> </dl>               | Argumento de ponteiro **nulo** .<br/>                                                                  |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de mídia inválido. O grupo não é um grupo de vídeos ou o arquivo de origem não tem nenhum fluxo de vídeo.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método localiza o arquivo de origem associado a *pSource*, recupera o tipo de mídia do primeiro fluxo de vídeo no arquivo e define o formato de compactação de grupo usando esse tipo. Para obter mais informações sobre formatos de compactação, consulte [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




