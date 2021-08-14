---
description: O método \_ put Filter especifica um filtro de origem para o detector de mídia usar.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: Método IMediaDet::p ut_Filter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a118baae251bd4456dfe0097afa091e0084e41ad96d96c9847006b8ce9c58d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398113"
---
# <a name="imediadetput_filter-method"></a>Método de filtro IMediaDet::p ut \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_Filter` método especifica um filtro de origem para o detector de mídia usar.

> [!IMPORTANT]
> Não adicione o filtro de origem ao seu próprio grafo de filtro ou use um filtro que já está em um grafo de filtro. O objeto do detector de mídia cria automaticamente um grafo de filtro interno e colocar o filtro em outro grafo pode causar resultados inesperados.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ Em\]
</dt> <dd>

Ponteiro para a interface **IUnknown** do filtro de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                   | Description                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *newVal* não aponta para um filtro.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Argumento de ponteiro **NULL.**<br/>           |



 

## <a name="remarks"></a>Comentários

Para a maioria dos aplicativos, é mais simples chamar o [**método \_ Filename IMediaDet::p ut**](imediadet-put-filename.md) com o nome de um arquivo de origem.

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

 

 




