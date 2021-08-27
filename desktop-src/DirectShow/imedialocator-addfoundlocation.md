---
description: O método AddFoundLocation adiciona um diretório ao cache de diretório.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: Método IMediaLocator::AddFoundLocation (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ba466338e6d148e3c39a6bed4f7db413ad444ee792a4fd49b6e1499f29f0403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051636"
---
# <a name="imedialocatoraddfoundlocation-method"></a>Método IMediaLocator::AddFoundLocation

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `AddFoundLocation` método adiciona um diretório ao cache de diretório.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DirectoryName* 
</dt> <dd>

Caminho do diretório a ser adicionar ao cache.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O localizador de mídia mantém um cache de caminhos de diretório em que ele encontrou arquivos com êxito em pesquisas anteriores. Quando ele localiza um arquivo com êxito, ele adiciona o diretório ao cache.

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

[**IMediaLocator Interface**](imedialocator.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




