---
description: Define ou recupera o \_ contexto PCCERT de um certificado.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'Propriedade ICertContext:: CertContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783237"
---
# <a name="icertcontextcertcontext-property"></a>Propriedade ICertContext:: CertContext

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

A propriedade **CertContext** define ou recupera o \_ contexto de PCCERT de um certificado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Valor da propriedade

O \_ contexto PCCERT do certificado.

## <a name="error-codes"></a>Códigos do Erro

Se os métodos de acesso à propriedade **colocarem \_ CertContext** e o **\_ CertContext** forem bem-sucedidos, eles retornarão S \_ OK.

Qualquer outro valor **HRESULT** indica que a chamada falhou.

## <a name="remarks"></a>Comentários

Você deve chamar o método [**FreeContext**](icertcontext-freecontext.md) ou a função [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) para liberar o contexto.

Se você definir a propriedade **CertContext** , o estado do objeto de [**certificado**](certificate.md) inteiro será redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




