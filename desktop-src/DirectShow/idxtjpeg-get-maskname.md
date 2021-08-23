---
description: O \_ método Get mascaraname recupera o nome de um arquivo JPEG a ser usado como a máscara de apagamento.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'Método IDxtJpeg:: get_MaskName (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d984f426289b9017ca316567b474beaa41b39a35f0ab012ea94ffdd8db33a36b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584736"
---
# <a name="idxtjpegget_maskname-method"></a>Método de IDxtJpeg:: obter \_ mascaraname

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_MaskName` método recupera o nome de um arquivo JPEG a ser usado como a máscara de apagamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe o nome do arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se a transição de apagamento estiver usando um dos apagamentos internos do SMPTE aos quais ele dá suporte, o valor dessa propriedade será uma cadeia de caracteres vazia.

O chamador deve liberar a cadeia de caracteres retornada, usando a função **SysFreeString** .

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

[**Interface IDxtJpeg**](idxtjpeg.md)
</dt> <dt>

[**IDxtJpeg:: obter \_ MaskNum**](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




