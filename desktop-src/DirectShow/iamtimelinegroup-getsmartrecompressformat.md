---
description: O método GetSmartRecompressFormat recupera o formato de compactação atual para a recompactação inteligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'Método IAMTimelineGroup:: GetSmartRecompressFormat (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8d568bdf0446533df9391c1c0b30382b9a56ecdf0ed788d64c48c38ddf0684a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400724"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a>Método IAMTimelineGroup:: GetSmartRecompressFormat

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetSmartRecompressFormat` método recupera o formato de compactação atual para a recompactação inteligente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppFormat* 
</dt> <dd>

Recebe um ponteiro para uma estrutura [**SCompFmt0**](scompfmt0.md) , convertida como um ponteiro para um longo. Se o método falhar, o valor será definido como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o aplicativo não tiver definido um formato de compactação inteligente (chamando [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), o formato retornado por esse método será inválido. Chame o método [**IAMTimelineGroup:: IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) para determinar se um formato de compactação foi definido.

Se o método for bem sucedido, o chamador deverá liberar o tipo de mídia retornado e excluir a estrutura [**SCompFmt0**](scompfmt0.md) :


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




