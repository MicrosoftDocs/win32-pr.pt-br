---
title: Configurando direitos de acesso em todo o objeto
description: Determinadas permissões podem ser definidas somente para um objeto inteiro, como excluir e listar conteúdo. Permissões específicas de operação, como a permissão de leitura, também podem ser definidas para o objeto inteiro para que se apliquem a um objeto inteiro.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Configurando direitos de acesso no AD do objeto inteiro
- AD de objetos, configurando direitos de acesso em
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde06726b7333865fe2f4b87b87bec4383a3aeb1799ad6b8772142d5b9fd6eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024774"
---
# <a name="setting-access-rights-on-the-entire-object"></a>Configurando direitos de acesso em todo o objeto

Determinadas permissões podem ser definidas somente para um objeto inteiro, como excluir e listar conteúdo. Permissões específicas de operação, como a permissão de leitura, também podem ser definidas para o objeto inteiro para que se apliquem a um objeto inteiro.

O procedimento a seguir pode ser usado para definir permissões para um objeto inteiro.

**Para definir permissões para um objeto inteiro**

1.  Defina [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ permitido** ou **ADS \_ AceType \_ acesso \_ negado**.
2.  Defina [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) e **IADsAccessControlEntry. InheritedObjectType** como **NULL**.

Para obter mais informações sobre como criar uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 