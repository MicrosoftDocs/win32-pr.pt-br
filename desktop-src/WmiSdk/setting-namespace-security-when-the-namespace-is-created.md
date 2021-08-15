---
title: Definindo a segurança na criação do namespace
description: O arquivo de formato MOF (MOF) que cria um namespace também pode definir os descritores de segurança para o namespace, incluindo o qualificador NamespaceSecuritySDDL com a descrição de segurança no formato SDDL (Security Descriptor Definition Language).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004e1897553ef2ec0bd57067b17d714f6aaf8b17059c1078a2fc0da8a060a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315633"
---
# <a name="setting-security-on-namespace-creation"></a>Definindo a segurança na criação do namespace

O arquivo de formato MOF (MOF) que cria um namespace também pode definir os descritores de [*segurança*](/windows/desktop/SecGloss/s-gly) para o namespace, incluindo o qualificador **NamespaceSecuritySDDL** com a descrição de segurança no formato [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .

Você pode usar o **NamespaceSecuritySDDL** para proteger qualquer namespace. Você também pode usar esse qualificador em um arquivo MOF simples para alterar o descritor de segurança em um namespace existente. A cadeia de caracteres SDDL é processada pelo WMI para estabelecer a segurança do namespace, mas não é armazenada como uma cadeia de caracteres. Se nenhum descritor de segurança for especificado, a segurança padrão será usada. Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).

O procedimento a seguir define o descritor de segurança para o namespace *\\ MyNamespace raiz* . A cadeia de caracteres SDDL define o proprietário e o grupo para usuários autenticados e especifica uma [*DACL (lista de controle de acesso discricionário)*](/windows/desktop/SecGloss/d-gly) que é herdada pelos namespaces filho. A DACL permite ao usuário o direito de ler dados, executar métodos, gravar dados em classes de provedor e usar o acesso remoto: **WBEM \_ habilitar**, **\_ método WBEM \_ Execute**, **\_ \_ provedor de gravação WBEM**, **\_ \_ acesso remoto WBEM**. Para obter mais informações, consulte [Access to WMI namespaces](access-to-wmi-namespaces.md).

**Para definir uma DACL de namespace**

1.  Crie um arquivo de formato MOF (MOF) ou modifique o arquivo MOF existente que define o namespace para adicionar o qualificador **NamespaceSecuritySDDL** com a cadeia de caracteres SDDL.

    O exemplo de código a seguir mostra que o namespace a ser modificado é root \\ MyNamespace e o arquivo é chamado MyNamespace \_ Security. mof.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Lembre-se de que a cadeia de caracteres SDDL diferencia maiúsculas de minúsculas: as letras devem estar em letras maiúsculas.

    O exemplo de código a seguir mostra as letras "o" e "g" na cadeia de caracteres SDDL como minúsculas e fará com que Mofcomp.exe retorne um erro.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  Execute [**Mofcomp.exe**](mofcomp.md) para compilar o arquivo MOF.

    **c: \\ Mofcomp MyNamespace \_ Security. mof**

    Em C++, use os métodos [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

4.  Se a tentativa de definir a DACL do namespace falhar, considere as seguintes mensagens de erro:

    

    | Erro                           | Descrição                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **parâmetro de WBEM \_ E \_ inválido \_** | Não há nenhuma DACL herdada. Como alternativa, o chamador violou a DACL ou o SD no namespace pai. |
    | **acesso ao WBEM \_ E \_ \_ negado**     | O chamador não tem permissão para atualizar o SDDL no MOF.                                               |

    

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo descritores de segurança de namespace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Constantes de direitos de acesso de namespace**](namespace-access-rights-constants.md)
</dt> <dt>

[**Constantes do sinalizador ACE do namespace**](namespace-ace-flag-constants.md)
</dt> <dt>

[Alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
