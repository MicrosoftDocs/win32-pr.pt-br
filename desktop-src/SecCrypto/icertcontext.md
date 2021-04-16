---
description: Fornece acesso ao contexto de um objeto de certificado CAPICOM X. 509v3. Esse contexto permite que o certificado capicor seja usado em outras derivações de CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Interface ICertContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758912"
---
# <a name="icertcontext-interface"></a>Interface ICertContext

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

A interface **ICertContext** fornece acesso ao contexto de um objeto de [**certificado**](certificate.md) CAPICOM X. 509v3. Esse contexto permite que o certificado capicor seja usado em outras derivações de CryptoAPI.

## <a name="when-to-use"></a>Quando usar

Use essa interface quando precisar usar um objeto de [**certificado**](certificate.md) capicor em outra derivação de CryptoAPI.

## <a name="members"></a>Membros

A interface **ICertContext** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **ICertContext** tem esses métodos.



| Método                                          | Descrição                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](icertcontext-freecontext.md) | Libera um \_ contexto PCCERT adquirido por meio da propriedade [**CertContext**](icertcontext-certcontext.md) .<br/> |



 

### <a name="properties"></a>Propriedades

A interface **ICertContext** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso           | Descrição                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**CertContext**](icertcontext-certcontext.md)<br/> | Leitura/gravação<br/> | Define ou recupera o \_ contexto PCCERT de um certificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




