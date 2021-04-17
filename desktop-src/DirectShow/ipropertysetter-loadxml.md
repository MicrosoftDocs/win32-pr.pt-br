---
description: O método LoadXML carrega dados de propriedade expressos em linguagem XML (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'Método IPropertySetter:: LoadXML (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754241"
---
# <a name="ipropertysetterloadxml-method"></a>Método IPropertySetter:: LoadXML

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `LoadXML` método carrega dados de propriedade expressos em linguagem XML (XML).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PXML* \[ no\]
</dt> <dd>

Ponteiro para a interface **IUnknown** de um elemento XML criado pelo Microsoft XML Parser.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                                  | Descrição                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>                      | Nenhum dado de propriedade.<br/>    |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                | Memória insuficiente.<br/> |
| <dl> <dt>**VFW \_ E \_ \_ formato de arquivo inválido \_**</dt> </dl> | Formato inválido.<br/>      |



 

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos não precisarão usar esse método. O DES o usa internamente para carregar Propriedades de arquivos XTL.

Para usar esse método, crie um objeto **IXMLDocument** e use-o para analisar um arquivo XML. Em seguida, use o objeto **IXMLDocument** para recuperar objetos **IXMLElement** . Se o objeto tiver Propriedades, você poderá passar o ponteiro **IXMLElement** para o método **LoadXml** . O método carrega as propriedades no setter da propriedade.

> [!Note]  
> As interfaces **IXMLDocument** e **IXMLElement** são implementadas no Microsoft XML Core Services (MSXML) versão 1,0, mas não são implementadas em versões mais recentes do MSXML.

 

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

 

 




