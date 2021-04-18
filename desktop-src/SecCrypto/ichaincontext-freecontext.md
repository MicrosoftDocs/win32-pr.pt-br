---
description: Libera um contexto de cadeia de PCCERT \_ \_ adquirido por meio da propriedade chainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'Método IChainContext:: FreeContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800081"
---
# <a name="ichaincontextfreecontext-method"></a>Método IChainContext:: FreeContext

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

O método **FreeContext** libera um contexto de cadeia de PCCERT \_ \_ adquirido por meio da propriedade [**chainContext**](ichaincontext-chaincontext.md) .

## <a name="syntax"></a>Sintaxe


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pChainContext* \[ no\]
</dt> <dd>

O contexto da cadeia de PCCERT \_ \_ a ser liberado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica êxito. Qualquer outro valor indica que a operação falhou.

## <a name="remarks"></a>Comentários

Esse método não libera o contexto de \_ cadeia de PCCERT \_ contido em um objeto de [**cadeia**](chain.md) . Ele deve ser usado apenas para liberar um contexto de cadeia de PCCERT \_ \_ adquirido por meio da propriedade [**chainContext**](ichaincontext-chaincontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




