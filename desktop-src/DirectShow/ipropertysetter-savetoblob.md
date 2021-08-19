---
description: O método SaveToBlob salva os dados de propriedade em um formato de persistência.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'Método IPropertySetter:: SaveToBlob (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c94cbb7b927e4bce7309e3e8a016b0e43bc6a0f9f3f319ee733e6e22132b47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952535"
---
# <a name="ipropertysettersavetoblob-method"></a>Método IPropertySetter:: SaveToBlob

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SaveToBlob` método salva os dados de propriedade em um formato de persistência.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcSize* \[ fora\]
</dt> <dd>

Recebe o tamanho dos dados, em bytes.

</dd> <dt>

*ppb* \[ fora\]
</dt> <dd>

Recebe um ponteiro para uma matriz de bytes que recebe os dados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O método aloca memória para a matriz de bytes. O chamador deve liberá-lo, usando a função **CoTaskMemFree** .

Todos os nomes de propriedade e valores são truncados para 40 caracteres de comprimento. Por esse motivo, XML é o formato de persistência preferencial. Consulte a [**interface IXml2Dex**](ixml2dex.md).

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

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




