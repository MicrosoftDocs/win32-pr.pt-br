---
description: O método get \_ Similarity recupera o intervalo de dados de cores que se torna transparente. Em valores mais altos, um intervalo maior de cores semelhantes é transparente. Essa propriedade se aplica somente quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: Método IDxtKey::get_Similarity (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dda31145fe28f0b428189eafd3105ae56120fbc19e0c611ad0df8d9f511130a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399136"
---
# <a name="idxtkeyget_similarity-method"></a>Método IDxtKey::get \_ Similarity

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_Similarity` método recupera o intervalo de dados de cores que se torna transparente. Em valores mais altos, um intervalo maior de cores semelhantes é transparente. Essa propriedade se aplica somente quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recebe o valor de similaridade.

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

[**IDxtKey Interface**](idxtkey.md)
</dt> <dt>

[**IDxtKey::get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




