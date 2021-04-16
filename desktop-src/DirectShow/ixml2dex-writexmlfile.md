---
description: O método WriteXMLfile converte uma linha do tempo em XML e grava os dados XML em um arquivo.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'Método IXml2Dex:: WriteXMLfile (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758837"
---
# <a name="ixml2dexwritexmlfile-method"></a>Método IXml2Dex:: WriteXMLfile

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `WriteXMLFile` método converte uma linha do tempo em XML e grava os dados XML em um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Ponteiro para a interface **IUnknown** do objeto de linha do tempo.

</dd> <dt>

*FileName* 
</dt> <dd>

Cadeia de caracteres que especifica o nome do arquivo a ser gravado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação da interface. O **HRESULT** pode incluir uma das seguintes constantes padrão ou outros valores não listados.



| Código de retorno                                                                                   | Descrição                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento inválido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>             |



 

## <a name="remarks"></a>Comentários

Esse método gera um arquivo XML que representa todos os componentes na linha do tempo.

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

 

 




