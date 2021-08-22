---
description: Define ou recupera o identificador HCERTSTORE de um repositório de certificados.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'Propriedade ICertStore:: StoreHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2858e7484c82663b2ba6866d0f17b5528921619dbfa80cbb76ec0eabbb39a332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005614"
---
# <a name="icertstorestorehandle-property"></a>Propriedade ICertStore:: StoreHandle

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

A propriedade **StoreHandle** define ou recupera o identificador HCERTSTORE de um repositório de certificados.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a>Valor da propriedade

O identificador HCERTSTORE do repositório de certificados.

## <a name="error-codes"></a>Códigos do Erro

Se os métodos de acesso à propriedade **colocarem \_ StoreHandle** e o **\_ StoreHandle** forem bem-sucedidos, eles retornarão S \_ OK.

Qualquer outro valor **HRESULT** indica que a chamada falhou.

## <a name="remarks"></a>Comentários

Você deve chamar o método [**CloseHandle**](icertstore-closehandle.md) ou a função [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) para liberar o contexto.

Se você definir a propriedade **StoreHandle** , o estado do objeto de [**loja**](store.md) inteiro será redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




