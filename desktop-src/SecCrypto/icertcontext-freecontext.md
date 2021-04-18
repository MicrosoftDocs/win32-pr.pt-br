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
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753401"
---
# <a name="icertcontextfreecontext-method"></a>Método ICertContext:: FreeContext

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

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

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica êxito. Qualquer outro valor indica que a operação falhou.

## <a name="remarks"></a>Comentários

Esse método não libera o contexto PCCERT \_ contido em um objeto de [**certificado**](certificate.md) . Ele deve ser usado apenas para liberar um \_ contexto PCCERT adquirido por meio da propriedade [**CertContext**](icertcontext-certcontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




