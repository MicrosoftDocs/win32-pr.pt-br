---
title: Propriedade ResourceLocator. FragmentDialect (WSManDisp. h)
description: Obtém ou define o dialeto de idioma para um dialeto de fragmento de recurso quando ResourceLocator é usado em operações de objeto de sessão, como Session. Get, Session. Put ou Session. Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade FragmentDialect
- Propriedade FragmentDialect Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, Propriedade FragmentDialect
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455835"
---
# <a name="resourcelocatorfragmentdialect-property"></a>Propriedade ResourceLocator. FragmentDialect

Obtém ou define o dialeto de idioma para um *dialeto* de [*fragmento*](windows-remote-management-glossary.md) de [*recurso*](windows-remote-management-glossary.md) quando [**ResourceLocator**](resourcelocator.md) é usado em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md). Um fragmento representa uma propriedade ou parte de um recurso. Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) . O dialeto indica qual linguagem XML descreve o fragmento para o serviço que implementa o [protocolo WS-Management](ws-management-protocol.md) e recebe a solicitação.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres XML que identifica o idioma usado na propriedade [**FragmentPath**](resourcelocator-fragmentpath.md) . A cadeia de caracteres de dialeto usa como padrão a especificação XPath 1,0. Para obter mais informações, confira [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Comentários

[**IWSManResourceLocator:: FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) é a propriedade C++ correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





