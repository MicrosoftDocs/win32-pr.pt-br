---
description: Você pode exigir que os scripts e aplicativos de cliente estabeleçam uma conexão criptografada para autenticação adicionando o qualificador RequiresEncryption ao arquivo MOF (formato MOF). MOF que cria o namespace.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Exigindo uma conexão criptografada para um namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763434"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a>Exigindo uma conexão criptografada para um namespace

Você pode exigir que os scripts e aplicativos de cliente estabeleçam uma conexão criptografada para autenticação adicionando o qualificador **RequiresEncryption** ao arquivo mof (formato MOF). MOF que cria o namespace.


Uma conexão criptografada com um namespace WMI especifica a **privacidade do PCT do \_ nível de \_ autenticação RPC \_ \_ \_ C** (ou **PktPrivacy** em um script) para autenticação. O qualificador **RequiresEncryption** faz com que o WMI rejeite quaisquer solicitações de dados de entrada, a menos que elas usem explicitamente a autenticação criptografada. Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md) ou definindo a [autenticação usando C++](setting-authentication-using-c-.md).

Você também pode modificar um namespace existente adicionando esse atributo e, em seguida, compilando o arquivo MOF novamente. **RequiresEncryption** é usado no [*MOF*](gloss-m.md) com a instrução de pré-processador do [namespace pragma](pragma-namespace.md) .

O procedimento a seguir define o namespace para exigir uma conexão criptografada.

**Para definir a criptografia necessária**

1.  Crie um arquivo de formato MOF (MOF) ou modifique o arquivo MOF existente que define o namespace.

    O exemplo de código a seguir mostra o namespace que será modificado como *root \\ MyNamespace* e o arquivo é chamado *MyNamespace \_ Security. mof*. **RequiresEncryption** tem um tipo de dados booliano para que ele deva ser definido como **true** ou **false**.

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  Execute [**mofcomp.exe**](mofcomp.md) para compilar o arquivo MOF.

    **c: \\ Mofcomp MyNamespace \_ Security. mof**

    Em C++, use os métodos [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

O WMI rejeita um cliente que usa o nível de autenticação padrão porque o DCOM negocia a segurança para o nível exigido pelo processo SVCHOST no qual o serviço WMI está em execução. Para obter mais informações sobre hosts de serviço, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md). Para obter mais informações sobre como configurar níveis de autenticação ao se conectar a namespaces do WMI, consulte [definindo o nível de segurança do processo padrão usando c++](setting-the-default-process-security-level-using-c-.md), [definindo a autenticação usando c++](setting-authentication-using-c-.md)ou [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

Ao retornar dados em uma conexão de retorno de chamada assíncrona, o WMI retorna uma mensagem de acesso negado ao computador solicitante. O WMI também faz uma entrada de log no log de eventos NT do computador com o namespace criptografado informando que não é possível estabelecer uma conexão segura com o cliente.

A partir do Windows Vista, o arquivo WbemCore. log não existe mais. Você pode verificar o log de eventos NT para entradas que indicam solicitações de dados de entrada rejeitadas para namespaces que exigem Criptografia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[Protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



