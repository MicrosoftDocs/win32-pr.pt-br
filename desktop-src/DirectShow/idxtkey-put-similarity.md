---
description: O método put \_ Similarity especifica o intervalo de dados de cores que se torna transparente. Em valores mais altos, um intervalo maior de cores semelhantes é transparente. Essa propriedade se aplica somente quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: Método IDxtKey::p ut_Similarity (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5dbd14b2791441f5c09a7242d6f8c1e343413f8c3cd94fc0519ac6487857b7d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399126"
---
# <a name="idxtkeyput_similarity-method"></a>Método de similaridade IDxtKey::p ut \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_Similarity` método especifica o intervalo de dados de cores que se torna transparente. Em valores mais altos, um intervalo maior de cores semelhantes é transparente. Essa propriedade se aplica somente quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ Em\]
</dt> <dd>

Especifica o valor de similaridade. O intervalo válido é de 0 a 100.

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

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




