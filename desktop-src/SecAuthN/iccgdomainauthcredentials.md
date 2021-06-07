---
description: Uma interface implementada pelo cliente que permite aos desenvolvedores fornecer suas próprias credenciais dinamicamente em tempo de execução para autenticar contêineres não ingressados no domínio com o Active Directory.
title: Interface ICcgDomainAuthCredentials (ccgplugins.h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387787"
---
# <a name="iccgdomainauthcredentials-interface"></a>Interface ICcgDomainAuthCredentials

Uma interface implementada pelo cliente que permite aos desenvolvedores fornecer suas próprias credenciais dinamicamente em tempo de execução para autenticar contêineres não ingressados no domínio com o Active Directory. 

## <a name="members"></a>Membros

A interface **ICcgDomainAuthCredentials** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ICcgDomainAuthCredentials** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ICcgDomainAuthCredentials** tem esses métodos.



| Método                                           | Descrição                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetPasswordCredentials**](iccgdomainauthcredentials-getpasswordcredentials.md)               | Retorna credenciais para autenticar um contêiner não ingressado no domínio com o Active Directory.<br/>                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente \[ aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>ccgplugins.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>ccgplugins.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ccgplugins.dll</dt> </dl> |
| IID<br/>                      | 6ecda518-2010-4437-8bc3-46e752b7b172<br/>          |



 

