---
description: para aprimorar a segurança do wmiprvse.exe processo de host do provedor compartilhado Instrumentação de Gerenciamento do Windows (WMI), foram feitas alterações em Windows plataformas que protegem o processo de host do provedor com um SID (identificador de segurança do serviço).
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Chaves e valores do registro para controlar a segurança do provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916a5910a6ad21e9f9dfdcfc0992de10ae30da82
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884358"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a>Chaves e valores do registro para controlar a segurança do provedor

para aprimorar a segurança do wmiprvse.exe processo de host do provedor compartilhado Instrumentação de Gerenciamento do Windows (WMI), foram feitas alterações em Windows plataformas que protegem o processo de host do provedor com um [*SID (identificador de segurança do serviço)*](gloss-s.md). Essas alterações apresentam os seguintes modos de execução para o host compartilhado do WMI: seguro e compatível.

As seções a seguir são abordadas neste tópico:

-   [Modos seguros e compatíveis](#secure-and-compatible-modes)
-   [Chaves e valores do registro](#registry-keys-and-values)
-   [Configurando um provedor para ser executado no modo seguro ou compatível](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a>Modos seguros e compatíveis

a partir do Windows 7, os dois modos de execução a seguir para o processo de host compartilhado WMI foram adicionados:

<dl> <dt>

<span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Modo de segurança
</dt> <dd>

Os recursos de processo do host do provedor WMI são protegidos com um [*Sid de serviço*](gloss-s.md). Somente o *SID do serviço* tem permissões para esses recursos.

</dd> <dt>

<span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Modo compatível
</dt> <dd>

O processo de host do provedor compartilhado WMI não está protegido com um [*Sid de serviço*](gloss-s.md). O processo host do provedor permite acesso às contas NetworkService ou LocalService, dependendo do modelo de hospedagem. Para obter mais informações sobre modelos de hospedagem, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).

</dd> </dl>

**Windows Vista e Windows Server 2008:** Para acessar as chaves e os valores do registro para controlar modos seguros e compatíveis para o processo de host do provedor, você deve instalar a atualização de segurança em [KB 959454](https://support.microsoft.com/kb/959454). Para obter mais informações, consulte o [Boletim de segurança da Microsoft MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).

## <a name="registry-keys-and-values"></a>Chaves e valores do registro

As configurações do modo seguro e compatível são especificadas por meio de chaves do registro. As chaves do registro para WMI estão localizadas no registro em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

As seguintes chaves do registro e o valor **DWORD** descritos na lista a seguir foram adicionados para controlar o comportamento dos provedores WMI.

<dl> <dt>

<span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**
</dt> <dd>

Essa chave controla o comportamento de provedores individuais. Todos os provedores listados nessa chave sempre são executados no modo de segurança. todos os provedores de caixa de entrada fornecidos com Windows são listados nessa chave e são executados no modo de segurança por padrão.

Essa chave tem precedência sobre os provedores listados na chave **CompatibleHostProviders** .

</dd> <dt>

<span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**
</dt> <dd>

Essa chave controla o comportamento de provedores individuais. Todos os provedores listados nessa chave sempre são executados no modo compatível. Essa chave está vazia por padrão.

Se um provedor estiver listado na chave **SecuredHostProviders** e na chave **CompatibleHostProviders** , o provedor será executado no modo de segurança.

> [!Note]  
> A chave **CompatibleHostProviders** fornece compatibilidade de aplicativos para aplicativos de terceiros se a chave **DefaultSecuredHost** estiver definida como 1 e o provedor não funcionar no modo de segurança.

 

</dd> <dt>

<span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**
</dt> <dd>

Um valor **DWORD** do registro global que determina se todos os provedores, que não estão listados nas chaves **SecuredHostProviders** ou **CompatibleHostProviders** , são executados no modo seguro ou compatível. Esse valor **DWORD** permite que o administrador decida em qual modo um provedor de terceiros deve ser executado. Por padrão, esse valor é definido como zero e todos os provedores de terceiros são executados no modo compatível. Os administradores podem tornar seu computador mais seguro por padrão, definindo o valor **DefaultSecuredHost** como 1.

> [!Note]  
> O valor de **DefaultSecuredHost** não afeta as outras chaves do registro. Os provedores listados na chave **SecuredHostProviders** permanecem no modo de segurança, e aqueles listados na chave **CompatibleHostProviders** permanecem no modo compatível.

 

As seguintes configurações são possíveis:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Especifica que os provedores são executados no modo compatível.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Especifica que os provedores são executados no modo de segurança.

</dd> </dl> </dd> </dl>

A lista a seguir lista as configurações de registro possíveis e os modos de execução associados para um provedor.



| Listado em SecuredHostProviders | Listado em CompatibleHostProviders | Configuração de DefaultSecuredHost | Mode       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| Não                                | Não                                   | 0                          | Compatível |
| Não                                | Sim                                  | 0                          | Compatível |
| Sim                               | Não                                   | 0                          | Seguro     |
| Sim                               | Yes                                  | 0                          | Seguro     |
| Não                                | Não                                   | 1                          | Seguro     |
| Não                                | Sim                                  | 1                          | Compatível |
| Sim                               | Não                                   | 1                          | Seguro     |
| Sim                               | Sim                                  | 1                          | Seguro     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a>Configurando um provedor para ser executado no modo seguro ou compatível

As chaves do registro podem ser modificadas usando o Console de Gerenciamento de Política de Grupo (GPMC). Para obter mais informações, consulte [console de gerenciamento de política de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Os procedimentos a seguir ilustram como gerenciar configurações de modo seguro e compatível usando as preferências de política de grupo. Para obter mais informações sobre as preferências de política de grupo, consulte a [visão geral de preferências de política de grupo](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).

**Para adicionar um provedor ao modo seguro ou compatível usando Política de Grupo**

1.  Abra o GPMC.
2.  Crie um objeto de Política de Grupo (GPO).
3.  Edite o GPO.
4.  navegue até preferências/Windows Configurações/Registry.
5.  Clique com o botão direito do mouse e selecione **novo... Registro**. Essa ação apresenta uma interface do usuário na qual você pode inserir informações do registro.
6.  Selecione o comando **criar** .
7.  Selecione o seguinte caminho de chave do registro:

    **Modo de segurança: hKey \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Modo compatível: hKey \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  No campo **nome** , insira o nome do provedor que você deseja adicionar a essa chave. O nome do provedor deve estar no seguinte formato: &lt; namespace &gt; : <\_ \_ RelPath>. Por exemplo, raiz \\ cimv2: \_ \_ Win32Provider. nome = "myfornecedor".
9.  No campo de **dados** , digite 0.
10. Clique em OK.

**Para remover um provedor do modo seguro ou compatível usando Política de Grupo**

1.  Abra o GPMC.
2.  Crie um GPO.
3.  Edite o GPO.
4.  navegue até preferências/Windows Configurações/Registry.
5.  Clique com o botão direito do mouse e selecione **novo... Registro**. Essa ação apresenta uma interface do usuário na qual você pode inserir informações do registro.
6.  Selecione o comando **remover** .
7.  Selecione o seguinte caminho de chave do registro:

    **Modo de segurança: hKey \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Modo compatível: hKey \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  No campo **nome** , insira o nome do provedor que você deseja remover dessa chave.
9.  No campo de **dados** , digite 0.
10. Clique em OK.

O procedimento a seguir fornece detalhes sobre como modificar o comportamento de provedores que não estão listados nas chaves **SecuredHostProviders** ou **CompatibleHostProviders** .

**Para alterar o valor padrão da chave DefaultSecuredHost usando Política de Grupo**

1.  Abra o GPMC.
2.  Crie um GPO.
3.  Edite o GPO.
4.  navegue até preferências/Windows Configurações/Registry.
5.  Clique com o botão direito do mouse e selecione **novo... Registro**. Essa ação apresenta uma interface do usuário na qual você pode inserir informações do registro.
6.  Selecione o comando **Atualizar** .
7.  Selecione o seguinte caminho de chave do registro: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.
8.  No campo **nome** , insira **DefaultSecuredHost**.
9.  No campo de **dados** , digite 0 para modo compatível ou 1 para modo de segurança.
10. Clique em OK.

 

 
