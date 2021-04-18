---
description: Fornece acesso ao contexto de um objeto de armazenamento capicor. Esse contexto permite que o repositório de certificados capicor seja usado em outras derivações de CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Interface ICertStore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789494"
---
# <a name="icertstore-interface"></a>Interface ICertStore

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

A interface **ICertStore** fornece acesso ao contexto de um objeto de [**armazenamento**](store.md) capicor. Esse contexto permite que o repositório de certificados capicor seja usado em outras derivações de CryptoAPI.

## <a name="when-to-use"></a>Quando usar

Use essa interface quando precisar usar um objeto de [**armazenamento**](store.md) capicor em outra derivação de CryptoAPI.

## <a name="members"></a>Membros

A interface **ICertStore** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **ICertStore** tem esses métodos.



| Método                                        | Descrição                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**CloseHandle**](icertstore-closehandle.md) | Fecha um identificador HCERTSTORE adquirido por meio da propriedade [**StoreHandle**](icertstore-storehandle.md) .<br/> |



 

### <a name="properties"></a>Propriedades

A interface **ICertStore** tem essas propriedades.



| Propriedade                                                     | Tipo de acesso           | Descrição                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**StoreHandle**](icertstore-storehandle.md)<br/>     | Leitura/gravação<br/> | Define ou recupera o identificador HCERTSTORE de um repositório de certificados.<br/>                                          |
| [**StoreLocation**](icertstore-storelocation.md)<br/> | Leitura/gravação<br/> | Define ou recupera o [**\_ \_ local de armazenamento capicor**](capicom-store-location.md) de um repositório de certificados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




