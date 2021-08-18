---
description: Libera um \_ contexto PCCERT adquirido por meio da propriedade CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'Método ICertContext:: FreeContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06809d8950d62f1136b8efc25c8e5b4499e020dce956d65f9e0d4a0e349567de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006184"
---
# <a name="icertcontextfreecontext-method"></a>Método ICertContext:: FreeContext

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

O método **FreeContext** libera um \_ contexto PCCERT adquirido por meio da propriedade [**CertContext**](icertcontext-certcontext.md) .

## <a name="syntax"></a>Sintaxe


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCertContext* \[ no\]
</dt> <dd>

O contexto de PCCERT \_ a ser liberado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica êxito. Qualquer outro valor indica que a operação falhou.

## <a name="remarks"></a>Comentários

Esse método não libera o contexto PCCERT \_ contido em um objeto de [**certificado**](certificate.md) . Ele deve ser usado apenas para liberar um \_ contexto PCCERT adquirido por meio da propriedade [**CertContext**](icertcontext-certcontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




