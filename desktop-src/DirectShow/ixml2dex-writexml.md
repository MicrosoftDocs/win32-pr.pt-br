---
description: O método WriteXML converte uma linha do tempo em uma cadeia de caracteres XML.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'Método IXml2Dex:: WriteXML (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782191"
---
# <a name="ixml2dexwritexml-method"></a>Método IXml2Dex:: WriteXML

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `WriteXML` método traduz uma linha do tempo para uma cadeia de caracteres XML.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Ponteiro para a interface **IUnknown** do objeto de linha do tempo.

</dd> <dt>

*pbstrXML* 
</dt> <dd>

Ponteiro para uma variável do tipo BSTR que recebe a cadeia de caracteres XML que descreve a linha do tempo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido. Se não houver memória suficiente para a conversão, retornará E \_ OUTOFMEMORY. Caso contrário, retorna outro código de erro.

## <a name="remarks"></a>Comentários

O método aloca memória para a cadeia de caracteres. O aplicativo deve chamar **SysFreeString** para liberar a memória.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Internet Explorer 4,0 ou posterior<br/>                                               |
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




