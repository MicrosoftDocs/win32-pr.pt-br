---
description: O método PrintXML converte dados de propriedade em uma cadeia de caracteres XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: 'IPropertySetter: método rintXML de:P (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812774"
---
# <a name="ipropertysetterprintxml-method"></a>IPropertySetter: método rintXML de:P

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `PrintXML` método converte dados de propriedade em uma cadeia de caracteres XML.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszXML* \[ fora\]
</dt> <dd>

Ponteiro para um buffer que recebe a cadeia de caracteres XML.

</dd> <dt>

*cbXML* \[ no\]
</dt> <dd>

Tamanho do buffer apontado por *pszXML*, em bytes.

</dd> <dt>

*pcbPrinted* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o comprimento da cadeia de caracteres XML. Pode ser **NULL**.

</dd> <dt>

*recuar* \[ no\]
</dt> <dd>

Número de níveis de recuo para a marca externa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido. Caso contrário, retorna um valor **HRESULT** que indica a causa do erro. Se a cadeia de caracteres XML for maior que o buffer, o método retornará E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

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

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




