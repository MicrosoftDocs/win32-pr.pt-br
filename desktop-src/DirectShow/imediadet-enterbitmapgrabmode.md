---
description: O método EnterBitmapGrabMode alterna o detector de mídia para o modo de captura de bitmap e busca o grafo de filtro em um horário especificado.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'Método IMediaDet:: EnterBitmapGrabMode (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d47989b95663a9a99f4363fb505aec996ea23acdd813cf301f7ee252c874dc78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952615"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>Método IMediaDet:: EnterBitmapGrabMode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `EnterBitmapGrabMode` método alterna o detector de mídia para o modo de captura de bitmap e procura o grafo de filtro em um horário especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Fluxo de transmissão* 
</dt> <dd>

Tempo, em segundos, para o qual o grafo busca.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                             | Descrição                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argumento inválido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | O arquivo de origem não tem um fluxo de vídeo.<br/> |
| <dl> <dt>**VFW \_ E \_ tempo \_ expirado**</dt> </dl>    | O comando de busca expirou.<br/>                       |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Esse método insere o filtro de [**apoio de exemplo**](sample-grabber-filter.md) no gráfico de filtro. Em seguida, você pode chamar [**IMediaDet:: GetSampleGrabber**](imediadet-getsamplegrabber.md) para obter um ponteiro para a interface [**ISampleGrabber**](isamplegrabber.md) . Depois que o detector de mídia entrar no modo de captura de bitmap, os vários métodos informativos no **IMediaDet** não funcionarão.

Os métodos [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md) também colocam o detector de mídia no modo de captura de bitmap.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

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

 

 




