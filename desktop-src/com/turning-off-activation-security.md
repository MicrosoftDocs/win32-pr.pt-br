---
title: Desativando a segurança de ativação
description: Desativando a segurança de ativação
ms.assetid: 3474f8ad-f041-4886-ad39-ff0603c5c69e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da3ebd7cc03d79fc38fbafe3bc652efc3499437
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366757"
---
# <a name="turning-off-activation-security"></a>Desativando a segurança de ativação

Normalmente, a ativação usa as configurações de segurança padrão. No entanto, você pode controlar a segurança de ativação especificando uma estrutura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) , que é um membro da estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) que é passada para as funções de ativação. Se o cliente especificar um nível de autenticação de RPC \_ C \_ Authn \_ \_ no nível None na estrutura **COAUTHINFO** , a autenticação não será tentada. Caso contrário, a ativação segura será tentada e, se a autenticação falhar, a ativação falhará.

Se o cliente não especificar uma estrutura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) explícita e, em vez disso, definir o ponteiro como **NULL**, com tentará autenticar o cliente. Se não for possível autenticar o cliente, o COM verificará o descritor de segurança de permissão de inicialização para ver se há uma DACL **nula** ou uma ACL que permite o acesso a todos. Se essa verificação for realizada com sucesso, o servidor será iniciado. Portanto, mesmo que o cliente não especifique uma estrutura **COAUTHINFO**, a ativação não segura poderá ocorrer quando o servidor permitir.

> [!Note]  
> Para permitir que usuários de rede não autenticados executem um aplicativo COM, as funções de aplicativo devem incluir o usuário anônimo. A partir do Windows Server 2003, por padrão, o usuário anônimo não está incluído no grupo Everyone.

 

Por que um cliente desejaria desativar a segurança de ativação explicitamente, embora a ativação não segura eventualmente ocorra se o servidor permitir? Como desativar explicitamente a segurança de ativação aumenta o desempenho quando o cliente não deseja ou precisa de verificações de segurança.

Os itens a seguir devem ser feitos para desativar explicitamente a segurança de ativação:

-   O cliente deve especificar um nível de autenticação de RPC \_ C \_ Authn \_ \_ no nível nenhum na estrutura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) que seja membro da estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) fornecida para a função de ativação.
-   O cliente deve especificar um nível de representação de \_ Impersonate de nível de Imp de RPC C \_ \_ \_ na estrutura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) que seja membro da estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) fornecida para a função de ativação. Se esse valor não for passado, você obterá o \_ servidor RPC S \_ \_ indisponível.
-   O servidor deve especificar **todos** para **as permissões de inicialização padrão**. A maneira recomendada para executar essa tarefa é usar Dcomcnfg.exe da seguinte maneira:
    1.  Execute Dcomcnfg.exe.
    2.  Na página **aplicativos** , selecione o aplicativo que representa o servidor. Clique no botão **Propriedades** (ou clique duas vezes no aplicativo selecionado).
    3.  Na página de propriedades **segurança** , clique no botão **usar permissões de inicialização personalizadas** .
    4.  Clique no botão **Editar** na área **permissões de inicialização** .
    5.  Na caixa de diálogo **permissões de valor do registro** , clique no botão **Adicionar** .
    6.  Selecione a entrada para **todos** na caixa de listagem.
    7.  Na caixa **de listagem tipo de acesso** , escolha **Permitir inicialização**.
    8.  Clique no botão **OK**.

> [!Note]  
> No Windows Server 2003, o recurso de autenticação para o aplicativo de sistema COM+ inclui o valor EOAC \_ Disable \_ AAA. Esse valor, que desabilita as ativações de Activate-as-Activator (AAA), é usado na chamada [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ao iniciar o aplicativo do sistema. Definir o recurso de autenticação como EOAC \_ Disable \_ AAA permite que um aplicativo executado em uma conta com privilégios (como LocalSystem) ajude a impedir que sua identidade seja usada para iniciar componentes não confiáveis.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desativando a segurança da chamada](turning-off-call-security.md)
</dt> </dl>

 

 