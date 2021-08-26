---
description: O método PrintXML converte dados de propriedade em uma cadeia de caracteres XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: Método IPropertySetter::P rintXML (Qedit.h)
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
ms.openlocfilehash: 5070a6906d7f30ab12171f551270f82b9851fa8c3990fade47aca6d2927509be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051506"
---
# <a name="ipropertysetterprintxml-method"></a>Método IPropertySetter::P rintXML

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

*pszXML* \[ out\]
</dt> <dd>

Ponteiro para um buffer que recebe a cadeia de caracteres XML.

</dd> <dt>

*cbXML* \[ Em\]
</dt> <dd>

Tamanho do buffer apontado por *pszXML*, em bytes.

</dd> <dt>

*pcbPrinted* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe o comprimento da cadeia de caracteres XML. Pode ser **NULL.**

</dd> <dt>

*recuo* \[ Em\]
</dt> <dd>

Número de níveis de recuo para a marca mais externa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido. Caso contrário, retornará **um valor HRESULT** indicando a causa do erro. Se a cadeia de caracteres XML for maior que o buffer, o método retornará E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

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

[**IPropertySetter Interface**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




