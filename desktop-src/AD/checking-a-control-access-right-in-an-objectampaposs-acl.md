---
title: Verificando um direito de acesso de controle na ACL de um objeto
description: Para verificar um direito de acesso de controle na ACL de um objeto, use a função AccessCheckByTypeResultList.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Verificando um direito de acesso de controle em um anúncio de ACL de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007355"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a>Verificando um direito de acesso de controle na ACL de um objeto

Para verificar um direito de acesso de controle na ACL de um objeto, use a função [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) . Para usar essa função, um aplicativo requer um ponteiro para o [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) do objeto em vez de uma interface [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) para um objeto com descritor de segurança ADSI.

Use as seguintes etapas para verificar o acesso de um direito de acesso controlado em um objeto:

1.  Obtenha um ponteiro de interface [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) para o objeto.
2.  Use o método [**IDirectoryObject:: Getobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para obter o descritor de segurança do objeto. O nome da propriedade que contém o descritor de segurança é [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor). A propriedade é retornada como um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .
3.  Use a estrutura do [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) com a função [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para verificar as permissões para o direito de acesso de controle especificado para o cliente especificado.

O código de exemplo no [código de exemplo para a verificação de um direito de acesso de controle na ACL de um objeto](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) mostra, em detalhes, como fazer isso.

 

 