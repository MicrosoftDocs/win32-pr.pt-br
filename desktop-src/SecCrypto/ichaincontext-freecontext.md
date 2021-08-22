---
description: Libera um CONTEXTO DE CADEIA PCCERT \_ adquirido por meio da propriedade \_ ChainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: Método IChainContext::FreeContext
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
ms.openlocfilehash: 10a6d0576cefd1c28e8f05fe455b89be90dcd36386b4312ef1921511616bce2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005484"
---
# <a name="ichaincontextfreecontext-method"></a>Método IChainContext::FreeContext

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

O **método FreeContext** libera um CONTEXTO DE CADEIA PCCERT \_ adquirido por meio da propriedade \_ [**ChainContext.**](ichaincontext-chaincontext.md)

## <a name="syntax"></a>Sintaxe


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pChainContext* \[ Em\]
</dt> <dd>

O CONTEXTO DE \_ CADEIA PCCERT \_ a ser liberado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **um HRESULT.** Um valor de S \_ OK indica êxito. Qualquer outro valor indica que a operação falhou.

## <a name="remarks"></a>Comentários

Esse método não libera o CONTEXTO DE CADEIA PCCERT \_ contido em um objeto \_ [**Chain.**](chain.md) Ele deve ser usado apenas para liberar um CONTEXTO DE CADEIA PCCERT \_ adquirido por meio da propriedade \_ [**ChainContext.**](ichaincontext-chaincontext.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




