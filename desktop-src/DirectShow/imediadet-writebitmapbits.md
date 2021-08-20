---
description: O método WriteBitmapBits recupera um quadro de vídeo no momento da mídia especificado e grava-o em um arquivo. O quadro de vídeo está sempre no formato RGB de 24 bits.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: Método IMediaDet::WriteBitmapBits (Qedit.h)
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
ms.openlocfilehash: fc2a967f5b0e99c50317e9dc226a4b345c6790a8ce2b6e5d42eb50dfdc3b105b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154151"
---
# <a name="imediadetwritebitmapbits-method"></a>Método IMediaDet::WriteBitmapBits

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método recupera um quadro de vídeo no momento da mídia `WriteBitmapBits` especificado e grava-o em um arquivo. O quadro de vídeo está sempre no formato RGB de 24 bits.

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

*StreamTime* 
</dt> <dd>

Hora em que recuperar o quadro de vídeo.

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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK, bem-sucedido. Caso contrário, **retornará um valor HRESULT** que indica a causa do erro. Os códigos de erro possíveis incluem o seguinte:



| Código de retorno                                                                                             | Descrição                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | Não foi possível adicionar o [**filtro Grabber de**](sample-grabber-filter.md) Exemplo ao grafo.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                  | Falha.<br/>                                                                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memória insuficiente.<br/>                                                                   |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>            | Erro inesperado.<br/>                                                                      |
| <dl> <dt>**STG \_ E \_ ACCESSDENIED**</dt> </dl>     | Não é possível substituir o arquivo.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de mídia inválido.<br/>                                                                    |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, de definir o nome do arquivo e o fluxo chamando [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream.**](imediadet-put-currentstream.md)

Esse método coloca o detector de mídia no modo de captura de bitmap. Depois que esse método for chamado, os vários métodos de informações de fluxo no **IMediaDet** não funcionarão, a menos que você crie uma nova instância do detector de mídia.

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

 

 




