---
title: Propriedade ResourceLocator.FragmentDialect (WSManDisp.h)
description: Obtém ou define o dialeto de idioma de um dialeto de fragmento de recurso quando ResourceLocator é usado em operações de objeto session, como Session.Get, Session.Put ou Session.Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Propriedade FragmentDialect Windows Gerenciamento Remoto
- Propriedade FragmentDialect Windows gerenciamento remoto, objeto ResourceLocator
- Objeto ResourceLocator Windows Gerenciamento Remoto, propriedade FragmentDialect
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
ms.openlocfilehash: b2ae7cbbd71b4ccad24ecaa17d0fd635761f661bcd6dc95ebc0345e9164adcd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997296"
---
# <a name="resourcelocatorfragmentdialect-property"></a>Propriedade ResourceLocator.FragmentDialect

Obtém ou define o [](windows-remote-management-glossary.md) [](windows-remote-management-glossary.md)  dialeto de idioma para um [](session.md) dialeto de fragmento de recurso quando [**ResourceLocator**](resourcelocator.md) é usado em operações de objeto session, [**como Session.Get**](session-get.md), [**Session.Put**](session-put.md)ou [**Session.Enumerate**](session-enumerate.md). Um fragmento representa uma propriedade ou parte de um recurso. Você pode fornecer um [**objeto ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em [**operações de**](session.md) objeto session. O dialeto indica qual linguagem XML descreve o fragmento para o serviço que implementa o protocolo WS-Management [e](ws-management-protocol.md) recebe a solicitação.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres XML que identifica o idioma usado na [**propriedade FragmentPath.**](resourcelocator-fragmentpath.md) A cadeia de caracteres de dialeto assume como padrão a especificação XPath 1.0. Para obter mais informações, confira [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Comentários

[**IWSManResourceLocator::FragmentDialect é**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) a propriedade C++ correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

 





