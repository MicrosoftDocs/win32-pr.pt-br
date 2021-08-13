---
title: Accesspermission
description: Descreve a ACL (Lista de Controle de Acesso) das entidades de segurança que podem acessar instâncias dessa classe. Essa ACL é usada apenas por aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- AccessPermission registry value COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641512d34b963879ceb3d1a6266a017836879b224b228edb3ad62d61300fb03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551340"
---
# <a name="accesspermission"></a>Accesspermission

Descreve a ACL (Lista de Controle de Acesso) das entidades de segurança que podem acessar instâncias dessa classe. Essa ACL é usada apenas por aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Comentários

Este é um **valor \_ BINARY** REG. Ele contém dados que descrevem a ACL (Lista de Controle de Acesso) das entidades de segurança que podem acessar instâncias dessa classe. Ao receber uma solicitação para se conectar a um objeto existente dessa classe, a ACL é verificada pelo aplicativo que está sendo chamado durante a representação do chamador. Se a verificação de acesso falhar, a conexão não será permitido. Se esse valor nomeado não existir, a ACL [**DefaultAccessPermission**](defaultaccesspermission.md) será testada para determinar se a conexão deve ser permitida.

Para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou não usam a interface [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) para especificar o AppID, o executável do binário do aplicativo deve ser mapeado para o AppID do aplicativo, conforme descrito em [**AppID**](appid.md). Isso é necessário para que COM possa localizar a AppID do aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Coinitializesecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 