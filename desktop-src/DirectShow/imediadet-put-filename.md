---
description: O método \_ put Filename especifica o nome do arquivo de origem para o detector de mídia usar.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: Método IMediaDet::p ut_Filename (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9a64c0232c77d732bd172bbd46e1a29eef57ae10a96cbaf2a581aeeec5100a20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398262"
---
# <a name="imediadetput_filename-method"></a>Método Filename IMediaDet::p ut \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_Filename` método especifica o nome do arquivo de origem para o detector de mídia a ser usado.

Não chame esse método duas vezes no mesmo objeto MediaDet. Para usar essa interface com mais de um arquivo de origem, crie instâncias separadas do objeto MediaDet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ Em\]
</dt> <dd>

Nome do arquivo da origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

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

[**IMediaDet Interface**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




