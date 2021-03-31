---
description: A maneira mais simples de criar um namespace é usar o código formato MOF (MOF) para criar o namespace dentro do diretório atual. O diretório atual é definido quando você faz logon.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Criando um namespace filho com código MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011964"
---
# <a name="creating-a-child-namespace-with-mof-code"></a>Criando um namespace filho com código MOF

A maneira mais simples de criar um namespace é usar o código formato MOF (MOF) para criar o namespace dentro do diretório atual. O diretório atual é definido quando você faz logon.

O procedimento a seguir descreve como criar um namespace filho usando o código MOF.

**Para criar um namespace filho usando o código MOF**

1.  Crie uma instância da classe [**\_ \_ namespace**](--namespace.md) .

    O exemplo de código a seguir mostra como criar um namespace filho.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  Se você quiser exigir que o usuário faça uma conexão criptografada com o namespace, use o qualificador **RequiresEncryption** . Para obter mais informações, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

    O exemplo de código a seguir mostra como exigir uma conexão criptografada.

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  Se você quiser definir um descritor de segurança no namespace em vez de usar a segurança de namespace padrão, use o qualificador **NamespaceSecuritySDDL** . Para obter mais informações, consulte [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md).

    O exemplo de código a seguir mostra como definir um descritor de segurança no namespace.

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  Compile e carregue a instância de [**\_ \_ namespace**](--namespace.md) usando o utilitário [Mofcomp](mofcomp.md) ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) . Tanto o Mofcomp quanto a interface **IMofCompiler** carregam automaticamente o namespace no diretório atual. Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Qualificadores WMI padrão**](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



