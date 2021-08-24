---
title: AccessPermission
description: Descreve a ACL (lista de controle de acesso) das entidades de segurança que podem acessar instâncias dessa classe. Essa ACL é usada somente por aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- COM valor do registro AccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641512d34b963879ceb3d1a6266a017836879b224b228edb3ad62d61300fb03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551340"
---
# <a name="accesspermission"></a>AccessPermission

Descreve a ACL (lista de controle de acesso) das entidades de segurança que podem acessar instâncias dessa classe. Essa ACL é usada somente por aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ binário reg** . Ele contém dados que descrevem a ACL (lista de controle de acesso) das entidades de segurança que podem acessar instâncias dessa classe. Após receber uma solicitação para se conectar a um objeto existente dessa classe, a ACL é verificada pelo aplicativo que está sendo chamado ao representar o chamador. Se a verificação de acesso falhar, a conexão não será permitida. Se esse valor nomeado não existir, a ACL [**DefaultAccessPermission**](defaultaccesspermission.md) será testada para determinar se a conexão deve ser permitida.

Para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou não usam a interface [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) para especificar a AppID, o executável do binário do aplicativo deve ser mapeado para a AppID do aplicativo, conforme descrito em [**AppID**](appid.md). Isso é necessário para que o COM possa localizar a AppID do aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 