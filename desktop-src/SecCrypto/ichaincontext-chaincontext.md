---
description: Define ou recupera o \_ \_ contexto de cadeia de PCCERT de um certificado.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'Propriedade IChainContext:: ChainContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761395"
---
# <a name="ichaincontextchaincontext-property"></a>Propriedade IChainContext:: ChainContext

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

A propriedade **chainContext** define ou recupera o \_ \_ contexto de cadeia de PCCERT de um certificado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Valor da propriedade

O \_ \_ contexto da cadeia de PCCERT do certificado.

## <a name="error-codes"></a>Códigos do Erro

Se os métodos de acesso à propriedade **colocarem \_ chainContext** e o **\_ chainContext** forem bem-sucedidos, eles retornarão S \_ OK.

Qualquer outro valor **HRESULT** indica que a chamada falhou.

## <a name="remarks"></a>Comentários

Você deve chamar o método [**FreeContext**](ichaincontext-freecontext.md) ou a função [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) para liberar o contexto.

Se você definir a propriedade **chainContext** , o estado do objeto de [**cadeia**](chain.md) inteiro será redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




