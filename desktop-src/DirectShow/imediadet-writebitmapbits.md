---
description: O método WriteBitmapBits recupera um quadro de vídeo no tempo de mídia especificado e o grava em um arquivo. O quadro de vídeo está sempre no formato RGB de 24 bits.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'Método IMediaDet:: WriteBitmapBits (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766992"
---
# <a name="imediadetwritebitmapbits-method"></a>Método IMediaDet:: WriteBitmapBits

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `WriteBitmapBits` método recupera um quadro de vídeo no tempo de mídia especificado e o grava em um arquivo. O quadro de vídeo está sempre no formato RGB de 24 bits.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Fluxo de transmissão* 
</dt> <dd>

Hora em que o quadro de vídeo será recuperado.

</dd> <dt>

*Largura* 
</dt> <dd>

Largura da imagem, em pixels.

</dd> <dt>

*Altura* 
</dt> <dd>

Altura da imagem, em pixels.

</dd> <dt>

*Filename* 
</dt> <dd>

Caminho do arquivo no qual salvar o bitmap. Se o arquivo já existir, esse método o substituirá.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK com êxito. Caso contrário, retorna um valor **HRESULT** que indica a causa do erro. Os códigos de erro possíveis incluem o seguinte:



| Código de retorno                                                                                             | Descrição                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOinterface**</dt> </dl>           | Não foi possível adicionar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ao grafo.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>                  | Falha.<br/>                                                                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memória insuficiente.<br/>                                                                   |
| <dl> <dt>**E \_ inesperado**</dt> </dl>            | Erro inesperado.<br/>                                                                      |
| <dl> <dt>**STG \_ E \_ ACCESSDENIED**</dt> </dl>     | Não é possível substituir o arquivo.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de mídia inválido.<br/>                                                                    |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Esse método coloca o detector de mídia no modo de captura de bitmap. Depois que esse método for chamado, os vários métodos de informações de fluxo no **IMediaDet** não funcionarão, a menos que você crie uma nova instância do detector de mídia.

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

 

 




