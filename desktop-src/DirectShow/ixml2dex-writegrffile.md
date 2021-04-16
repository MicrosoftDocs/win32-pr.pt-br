---
description: O método WriteGrfFile grava um grafo de filtro em um arquivo no formato. GRF.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'Método IXml2Dex:: WriteGrfFile (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779840"
---
# <a name="ixml2dexwritegrffile-method"></a>Método IXml2Dex:: WriteGrfFile

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `WriteGrfFile` método grava um gráfico de filtro em um arquivo no formato. GRF.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGraph* 
</dt> <dd>

Ponteiro para a interface **IUnknown** do grafo de filtro.

</dd> <dt>

*FileName* 
</dt> <dd>

Cadeia de caracteres que especifica o nome do arquivo a ser gravado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação da interface. HRESULT pode incluir uma das seguintes constantes padrão ou outros valores não listados.



| Código de retorno                                                                                  | Descrição                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>       | Falha.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>             |



 

Esse método também pode retornar códigos de erro gerados por chamadas internas para os métodos **IStorage:: CreateStream** e **IPersist:: Save** . Para obter mais informações, consulte o SDK da plataforma.

## <a name="remarks"></a>Comentários

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

 

 




