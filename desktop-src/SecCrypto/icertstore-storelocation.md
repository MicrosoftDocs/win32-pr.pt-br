---
description: Define ou recupera o \_ local de armazenamento CApicor \_ de um repositório de certificados.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'Propriedade ICertStore:: StoreLocation'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769281"
---
# <a name="icertstorestorelocation-property"></a>Propriedade ICertStore:: StoreLocation

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

A propriedade **StoreLocation** define ou recupera o [**\_ \_ local de armazenamento capicor**](capicom-store-location.md) de um repositório de certificados.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valor da propriedade

O local do repositório de certificados.

## <a name="error-codes"></a>Códigos do Erro

Se os métodos de acesso à propriedade **colocarem \_ StoreLocation** e o **\_ StoreLocation** forem bem-sucedidos, eles retornarão S \_ OK.

Qualquer outro valor **HRESULT** indica que a chamada falhou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




